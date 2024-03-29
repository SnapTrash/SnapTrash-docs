# Database schema
Rules:
- camelCase for collections
- snake_case for fields


## users
- name: string
- full_name: string
- status : number
- profile_image : string (idReference to file in Storage)
- id_association: string
- isAdmin: bool
- private
  - birth_date : timestamp
  - sex : number (male = 0, female = 1, unspecified = 2)
  - phone_number : string
  - email: string
- pointsHistory 
  - date : timestamp
  - value : number
  - topic : string
  - message : string
- gifts
  - id_gift : string (idGift reference to gifts )
  - date : timestamp
- badges
  - id_badge : string (idBadge reference to badges)
  - date : timestamp
- friends
  - status: number
  - id_user : string (idUser references to users)
  - date : timestamp
- status : number (status of the profile, ex. 1 = active, 0 = deactive)
- reports
  - date : timestamp
  - id_association : string
  - association_id_user : string (login)
  - message: string
  - status: number
  - reason : string

## gifts
- name : string
- code_product : string
- supplier_name : String
- number_of_gift_available : number 
- start_number_of_gift : number
- price : number
- id_image_gift : string (idReference in giftImages in Storage)

## badges 
- name : string 
- id_image_badge : string (idReference in badgeImages in Storage)

## snaps
 - coordinates : geopoint (latitude and longitude as number)
 - user : string
 - date : timestamp
 - id_snap_image : string (idReference in snapImages in Storage)
 - description : string
 - urgency : number (1= low urgency , 3 = high urgency)
 - area: string
 - associationWritable
  - confirmed_urgency : number
  - status : number (0 = not cleaned , 1 = cleaned, 2 = not present)
## locationAreas
- country : string
- region : string
- municipality : string
- authorizedAssociations
  - id_association : string (idAssociation references to associations)
 
## associations
- name : string
- phone_number : string
- email : string
- type : string
- country : string
- city : string
- zip_code : string
- street_number : string (can have letter ex 10b)
- locationAreasWorking
  - id_location_areas : string (idReference in locationAreas)
- members
  -  user: reference
- payments
  - date : timestamp
  - amount : number
  - purpose : string
  - invoice : string (idReference in parcels in Storage)

 ## wasteDisposalCenters (optional)
- name : string
- phone_number : string
- email : string
- country : string
- city : string
- zip_code : string
- street_number : string (can have letter ex 10b)
- locationAreasWorking
  - id_location_area : string (idReference in locationAreas)
- typeWaste 
  - name_type : string
  
 

# Storage

## snapImages
## userProfileImages
## giftImages
## badguser: references
