# Database schema
Rules:
- camelCase for collections
- snake_case for fields


## users
- name : string
- surname : string
- birth_date : timestamp
- sex : number (male = 0, female = 1, unspecified = 2)
- username : string
- phone_number : string
- email: string
- password : string
- status : number
- profile_image : string (idReference to file in Storage)
- snaps
  - id_snap : string (idSnapReference to snaps under locationAreas)
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
  id_user : string (idUser references to users)
  date : timestamp
- status : number (status of the profile, ex. 1 = active, 0 = deactive)
- reports
  - date : timestamp
  - association_name : string
  - association_user : string (login)
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

## locationAreas
- country : string
- region : string
- municipality : string
- snaps
  - coordinates : geopoint (latitude and longitude as number)
  - country : string (has to be the same of the locationArea)
  - region : string (has to be the same of the locationArea)
  - municipality : string (has to be the same of the locationArea)
  - user : string ( idReference to users)
  - date : timestamp
  - id_snap_image : string (idReference in snapImages in Storage)
  - description : string
  - urgency : number (1= low urgency , 3 = high urgency)
  - confirmed_urgency : number
  - confirmed_presence : number (1 = present, 0 = not present)
  - status : number (ex. 0 = not cleaned , 1 = cleaned)
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
  - idLocation_areas : string (idReference in locationAreas)
- LoginUsers
  - name : string
  - surname : string
  - login_name : string
  - password : string
  - type : string
  - phone_number : string
- payments
  - date : timestamp
  - amount : number
  - purpose : string
  - parcel : string (idReference in parcels in Storage)


## admins
- name : string
- surnaname : string
- email: string
- password : string
- role : string
- phone_number : string

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
## badgeImages
## parcels
