# Meeting logs
## 24.03.2023 [Week 2]
### Agenda
- Finalizing database schema
- Setting up server-side infrastructure
- Finalizing functionality
- Specification doc
- Creating code style rules
### Presence
- [x] Giorgio Gueli
- [x] Hany Ghorbel
- [x] Patrik Fábián
- [x] Tobias Kolbe
### Meeting log
#### Finalizing functionality
- We were looking at the *funcionality.md* document
- We went over the functions and discussed them, often carrying over to the database
- We agreed not to address every problem we could find with respect to the timeframe
- See commits: d17894ffd895ad6bcf2b7a5d68d4b100b0647506 c64b67f8bc81d25c275e71b036af0df2ad625a15 1d5673b5eacf587a25378b221cf8dd5759bbb65f
#### Database schema
- Depends on the functionality too much, will be finalized next day (25.03)
#### Code style
- We've agreed on the following:
- Kotlin code: see https://kotlinlang.org/docs/coding-conventions.html
- Database naming conventions: camelCase for collections, snake_case for fields
- Will create a different Markdown file
#### Specification document
- Hany will finish the document during the project using the functionality document 
#### Setting up server-side infrastructure
- Firestore and Firebase Storage will be used
- Giorgio will be the infra owner for now
#### UI/UX
- Giorgio and Tobias will continue drawing mockups

### Summary
- See pull requests #16 and #17, which contain most of this meeting's progress

## 04.04.2023 [Week 4]
### Agenda
- Required database changes
- How to interact with backend
- UI progress
- Goals for this week
### Presence
- [x] Giorgio Gueli
- [x] Hany Ghorbel
- [x] Patrik Fábián
- [x] Tobias Kolbe
### Meeting log
#### Required database changes
Agreed on all of the changes from pull request #23.
Settlements will be used instead of municipalities for the areas.
#### How to interact with backend
Function calls and cloud triggers have been explained to the responsible team member.
#### UI progress
@GioGue implemented the login screen.
The logo has been finalized and merged into the docs repo (pull request #24).
#### Goals for this week
- Completion of the user and snap handling on the server-side
- Completion of the register, login screens, with a simple home page for the logged in user
- Registration will be a cloud function, normal client-side reg will be disabled.
- Segmentation and competitor analysis will be worked on this week (probably on Wednesday)
## 18.04.2023 [Week 6]
### Agenda
- CameraX support
- Database schema changes
- Smaller UI changes
- OSMDroid
- UI-VM integration
- "Office" hours
- Carbonara recipe
### Presence
- [x] Giorgio Gueli
- [x] Hany Ghorbel
- [x] Patrik Fábián
- [x] Tobias Kolbe
### Meeting log
#### CameraX
@GioGue will work on this, more team members may be required to solve more difficult problems.
#### UI changes
Settings will be "Account settings".
#### OSMDroid
@hanyghorbel will work on the map.
#### Database
Snaps will be moved up to the root of the whole database.
#### Working hours
We're going to work together 09-17.
#### How to make carbonara
[SECRET]
