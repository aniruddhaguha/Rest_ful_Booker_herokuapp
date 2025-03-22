# Restful Booker API Testing

## Overview
This repository contains a Postman collection for testing the Restful Booker API. The collection includes various API requests for managing hotel bookings, authentication, and modifying bookings.

## Prerequisites
- [Postman](https://www.postman.com/downloads/)
- A valid internet connection

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/Restful_Booker_API_testing.git
   ```
2. Open Postman and import the `Rest_ful_Booker_herokuapp.postman_collection.json` file.

## Collection Details
This collection contains the following requests:

1. **Get All Bookings**  
   - Method: `GET`  
   - URL: `{{base_url}}/booking`  
   - Purpose: Retrieves a list of all bookings.

2. **Get Booking by ID**  
   - Method: `GET`  
   - URL: `{{base_url}}/booking/{id}`  
   - Purpose: Fetches booking details for a specific ID.

3. **Create a New Booking**  
   - Method: `POST`  
   - URL: `{{base_url}}/booking`  
   - Body:
     ```json
     {
       "firstname": "Jim",
       "lastname": "Brown",
       "totalprice": 111,
       "depositpaid": true,
       "bookingdates": {
         "checkin": "2018-01-01",
         "checkout": "2019-01-01"
       },
       "additionalneeds": "Breakfast"
     }
     ```  
   - Purpose: Creates a new hotel booking.

4. **Generate Authentication Token**  
   - Method: `POST`  
   - URL: `{{base_url}}/auth`  
   - Body:
     ```json
     {
       "username": "admin",
       "password": "password123"
     }
     ```  
   - Purpose: Generates an authentication token for authorized actions.

5. **Update an Existing Booking**  
   - Method: `PUT`  
   - URL: `{{base_url}}/booking/{id}`  
   - Headers:
     ```json
     {
       "Cookie": "token=a0681f95e21de2b"
     }
     ```  
   - Body:
     ```json
     {
       "firstname": "Anirudha",
       "lastname": "Vai",
       "totalprice": 111,
       "depositpaid": true,
       "bookingdates": {
         "checkin": "2018-01-01",
         "checkout": "2019-01-01"
       },
       "additionalneeds": "midnight snack, lunch, dinner, Breakfast, snacks"
     }
     ```  
   - Purpose: Updates an existing booking with new details.

## Environment Variables
The collection uses the following variable:
- `base_url`: `https://restful-booker.herokuapp.com`

## Running Tests
1. Open Postman and navigate to the **Restful Booker API Testing** collection.
2. Select a request and click **Send** to execute.
3. Observe the response data to verify expected results.

