### User Registration and Login - UC-01

| **Use Case ID**     | **UC-01**                                                           | 
|---------------------|-------------------------------------------------------------------- |
| Actors              | Artist, Venue Owner                                                 |
| Description.        | Allows users to sign up and log in using email or social accounts.  |
| Precondition        | User must have a valid email.                                       |
| Postcondition       | User account is created, and user is redirected to their dashboard. |


#### Steps	

1. User clicks "Sign Up" button.  
2. Selects role — Artist or Venue Owner.  
3. Fills basic information. (For artist I will display full form and for venuw onwers I will later )  
4. System validates data and stores it in the database.  
5. User logs in successfully.  

### Artist Profile Management - UC-02

| **Use Case ID**     | **UC-02**                                                                  | 
|---------------------|----------------------------------------------------------------------------|
| Actors              | Artist                                                                     |
| Description         | Allows artists to create and manage their personal profiles and portfolios.|
| Precondition        |  User must be logged in.                                                   |
| Postcondition       | Updated artist profile is visible to venue owners.                         |


#### Steps		

1. Artist can update profile. 
2. System validates and updates information.  
3. Profile appears in artist directory.  

### Venue Listing Management - UC-03

| **Use Case ID**         | **UC-02**                                                                  | 
|-------------------------|----------------------------------------------------------------------------|
| Actors                  | Actors                                                                     |
| Description             | Allows venue owners to create, update, and manage venue listings.          |
| Precondition            | Venue owner must be logged in.                                             |
| Postcondition           | Venue appears in venue listings.                                    |


#### Steps

1. Venue owner clicks “Add Venue”.
2. Enters venue details (name, address, capacity, category, price, amenities).
3. System saves listing and displays it to artists.   