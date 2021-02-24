This project is based on [Udemy Rasa tutorial](https://www.udemy.com/course/rasa-for-beginners).

In the project root, create `.env` file:

```
AIRTABLE_API_KEY=key*****
BASE_ID=app*****
TABLE_NAME=Table%201
```

To use with Twilio:
* in the first terminal run: `rasa run`, 
* in the second terminal run: `rasa run actions`, 
* in the third terminal run: `ngrok http 5005` (or whatever port is Rasa Open Source server running on)
* create a Twilio number
* specify it in `credentials.yml`
* in Twilio -> Phone Numbers -> click your number -> Messaging -> set 
  "A message comes in" Webhook to `https://ae88d37d25d1.ngrok.io/webhooks/twilio/webhook`
  (or whatever address ngrok generated)
