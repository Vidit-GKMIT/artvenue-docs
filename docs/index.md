# Art Venue
This is a platform where artists and venue owners meet and grow. Here venue owners can find world's best artists, who can perform at your venue. And artists can find 5 star venues to perform at.

## Business Use Case
ArtVenue is a web platform designed to bridge the gap between artists seeking performance opportunities and venue owners looking to host talent.
The goal is to simplify the discovery, communication process between both communities.

## Business Objectives

1. To create a platform connecting artists and venue owners.  
2. To streamline the artist selection process.  
3. To enhance visibility for emerging artists.  
4. To help venue owners discover and hire high-quality performers.  

## Tech Stack

1. **Frontend:** - React.js (Vite)
2. **Banckend:** - Node.js and Express
3. **Database:** - PostgreSQL
4. **ORM** - Prisma
5. **Caching** - Redis for OTP storage

## Future Scope

1. **Choice for Venue Owner:** Venue owner can make choice on his own, to whom he need to select as performer. It can be done by when multiple artists see the venue they can just opt in and venue owner can go to it's event and see the available people who logged in.
2. **Venues can approach:** Restaurants can even approach to artists to perform.
3. **Venue owner can have multiple venues:** Now venue owner can list only 1 venue but in future scope there can be multiple venues added.
4. **History:** There can be performance history of artist so venue owners can go through it.

## Some Constraints

1. **Venue:** Venue can only be of type Hotel, Restaurant, Bar, Club to ensure data validation because if it's not there anyone can enter anything in venue type. Verification of venue done at server level.

2. **Artist:** Artist can only be type of Dance, Singing, Magician, Comedian, Videographer to ensure data vaildation because if it's not there annyone can enter anything in artist category. Verification of artist is done at server level.


<!-- ## Table of Contents  

- [Functional Document](functional_document.md)
- [Use Case Document](usecase_document.md)
- [Data Flow Diagram](data_flow_diagram.md) -->