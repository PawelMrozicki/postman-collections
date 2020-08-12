# Sabre Booking Management API Postman files

The Booking Management API (integral part of Sabre's Business Services) facilitates working with Sabre reservations (bookings) by providing a normalized set of services for the most common travel related use-cases.

## Current Release 

The services available in this API are listed below:

| Service | Description | Endpoint | Type |  
|---------|-------------|----------|------|
|[Get Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Normalized view of the Sabre Booking | /trip/orders/getBooking |RPC/JSON|
|[Get Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Normalized view of the Sabre Booking | /trip/orders/getBooking/graphql |GraphQL|
|[Cancel Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Normalized cancel of Sabre Products within a Booking| /trip/orders/cancelBooking |RPC/JSON|
|[Cancel Flight Tickets](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Normalized cancel(void/refund) for flight tickets and electronic miscellaneous documents (EMD)| /trip/orders/cancelBooking |RPC/JSON|


This Postman collection was created to showcase Sabre APIs and provide developers the ability to test them freely.

> Note: Sabre APIs Test credentials are required to successfully test these APIs, if you are an existing Sabre APIs customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install:

* [Postman](https://www.postman.com/) app

You'll also need your [Sabre APIs CERT-environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/)

### Installing

Here are one-time steps for getting your test environment set up:

* Run the Postman app on your local development machine 
* Import the [environment file](https://github.com/SabreDevStudio/postman-collections/blob/master/Sabre-APIs/Sabre_APIs_CERT.postman_environment.json) into Postman using the File -> Import option
* Import the [Booking Management Collection](./Booking_Management_API_v2020.04.postman_collection.json) into Postman using the File -> Import option 

### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your SOAP API credentials. The following variables have been marked out with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - also known as pseudo city code (your agency's unique identifier)

Update the dummy values with your official credentials. To do that follow these steps:

  * Click the gear icon to go to the manage environments pop-up dialog box.
  * Click on the name of your imported environment file to see a list of all key/value pairs.
  * Enter your credentials, and press the "Update" button.    

![environment varaibles](https://github.com/SabreDevStudio/postman-collections/blob/master/Sabre-APIs/postman_environ_vars.jpg)

## Running the Tests

1. Authenticate. In the Booking Management API collection you'll find a folder named `Authentication` and an item called `REST Authorize`. Select it. Click the **Send** button. Look for a 200 Success result. If it failed review your environment credentials.
2. Both the GetBooking and CancelBooking services require a confirmation id (PNR locator) in order to properly function, make sure you have one available in order to test. Examples are available in the individual folders: `Get Booking` and `Cancel Booking`. Simply open one of these folders, select an example to test, click the **Send** button, and look for a 200 Success result. 

For more information regarding our Booking Management API offering please [read through its documentation.](https://developer.sabre.com/) 

## License

Copyright (c) 2020 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.
