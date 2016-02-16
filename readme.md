# twiliochat-servlets
[![Build Status](https://travis-ci.org/TwilioDevEd/twiliochat-servlets.svg?branch=master)](https://travis-ci.org/TwilioDevEd/twiliochat-servlets)

Laravel implementation of Twilio Chat

### Run the application

1. Clone the repository and `cd` into it.
1. Copy the sample configuration file and edit it to match your configuration.

   ```bash
   $ cp .env.example .env
   ```

  You can find your `TWILIO_ACCOUNT_SID` in your
  [Twilio Account Settings](https://www.twilio.com/user/account/settings).
  For `TWILIO_API_KEY` and `TWILIO_API_SECRET` you need to go
  [here](https://www.twilio.com/user/account/ip-messaging/dev-tools/api-keys). There
  youl'll be able to create a new API key obtaining the two required values.
  For `TWILIO_IPM_SERVICE_SID` you can go [here](https://www.twilio.com/user/account/ip-messaging/services),
  where you must create an IP Messaging Service. When the service is created you'll
  have access to the service's SID.
1. Load the configuration file:

   ```bash
   $ source .env
   ```

1. Run the application using gretty gradle plugin.

  ```bash
  $ ./gradlew appRun
  ```

  Now you can access the application at `http://localhost:8080/twiliochat-servlets`.

## Expose your localhost to the internet

If you want your chat application to be reachable publicly in the internet, you can use
a service like [ngrok](https://ngrok.com/).

1. Expose the application to the wider Internet

   ```bash
   $ ngrok http 8080
   ```

### Dependencies

This application uses this Twilio helper library:
* [twilio-php](https://www.twilio.com/docs/php/install)

### Run the tests

1. Run at the top-level directory:

   ```bash
   $ ./gradlew test
   ```

1. Run javascript tests:
   ```bash
   $ cd src/main/webapp/ && npm install && npm test
   ```