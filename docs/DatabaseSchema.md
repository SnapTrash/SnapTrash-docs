# Database schema

## users
- name : string
- surname : string
- birthDate : timestamp
- sex : number (male = 0, female = 1, unspecified = 2)
- username : string
- phoneNumber : string
- email: string
- password : string
- status : number
- profileImage : string (idReference to file in Storage)
- snaps
  - idSnap : string (idSnapReference to snaps under locationAreas)
- pointsTotal : number
- pointsHistory 
  - date : timestamp
  - value : number
  - topic : string
  - message : string
- gifts
  - idGift : string (idGift reference to gifts )
  - date : timestamp
- badges
  - idBadge : string (idBadge reference to badges)
  - date : timestamp
- friends
  idUser : string (idUser references to users)
  date : timestamp
- status : number (status of the profile, ex. 1 = active, 0 = deactive)

## gifts
- name : string
- codeProduct : string
- supplierName : String
- numberOfGiftAvailable : number 
- startNumberOfGift : number
- imageBedge : string (idReference in giftImages in Storage)

## badges 
- name : string 
- idImageBadgeRef : string (idReference in badgeImages in Storage)

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
  - idSnapImage : string (idReference in snapImages in Storage)
  - description : string
  - status : number (ex. 0 = not cleaned , 1 = cleaned)
- authorizedAssociations
  - idAssociation : string (idAssociation references to associations)
 
## associations
- name : string
- phoneNumber : string
- email : string
- type : string
- country : string
- city : string
- zipCode : string
- streetNumber : string (can have letter ex 10b)
- locationAreasWorking
  - idLocationAreas : string (idReference in locationAreas)
- LoginUsers
  - name : string
  - surname : string
  - loginName : string
  - password : string
  - type : string
  - phoneNumber : string
- payments
  - date : timestamp
  - amount : number
  - purpose : string
  - parcel : string (idReference in parcels in Storage)


 ## wasteDisposalCenters (optional)
- name : string
- phoneNumber : string
- email : string
- country : string
- city : string
- zipCode : string
- streetNumber : string (can have letter ex 10b)
- locationAreasWorking
  - idLocationAreas : string (idReference in locationAreas)
- typeWaste 
  - nameType : string
  
 



# Storage

## snapImages
## userProfileImages
## giftImages
## badgeImages
## parcels
