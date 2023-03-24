# Meeting logs
## 2023.03.24 [Week 2]
### Agenda
- Finalizing database schema
- Setting up server-side infrastructure
- Finalizing functionality
- Specification doc
- Creating code style rules
## Presence
- [x] Giorgio Gueli
- [x] Hany Ghorbel
- [x] Patrik Fábián
- [x] Tobias Kolbe
## Meeting topics
### Finalizing functionality
- We were looking at the *funcionality.md* document
- We went over the functions and discussed them, often carrying over to the database
- We agreed not to address every problem we could find with respect to the timeframe
- See commits: d17894ffd895ad6bcf2b7a5d68d4b100b0647506 c64b67f8bc81d25c275e71b036af0df2ad625a15 1d5673b5eacf587a25378b221cf8dd5759bbb65f
### Database schema
- Depends on the functionality too much, will be finalized next day (25.03)
### Code style
- We agreed on the following:
- Kotlin code: see https://kotlinlang.org/docs/coding-conventions.html
- Database naming conventions: camelCase for collections, snake_case for fields
- Will create a different Markdown file
### Specification document
- Hany will finish the document during the project using the functionality document 
## Setting up server-side infrastructure
- Firestore and Firebase Storage will be used
- Giorgio will be the infra owner for now
## UI/UX
- Giorgio and Tobias will continue drawing mockups

## Summary
- See pull requests #16 and #17, which contain most of this meeting's progress
