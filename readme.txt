Slack integration : https://www.analyticsvidhya.com/blog/2019/04/learn-build-chatbot-rasa-nlp-ipl/
required credentials : 
    slack_token

to run: 
    python -m rasa_core.run -d models/current/dialogue -u models/current/nlu --port 5002 --connector slack --credentials slack_credentials.yml --endpoints endpoints.yml

if you get authorization errors:
    check for updated api formats and change slack.py code accordingly or get updated versions.

-------------------------------------------------------------------------------------------------------------------------
Whatsapp integration : Slack integration + https://medium.com/@alfredpfrancis/integrate-rasa-with-whatsapp-1b1477b51090
required credentials : 
    account_sid
    auth_token
    twilio_number: "whatsapp:+14155238886"

to run: 
    python -m rasa_core.run -d models/current/dialogue -u models/current/nlu --port 5002 --connector "twilio" --credentials slack_credentials.yml --endpoints endpoints.yml

-------------------------------------------------------------------------------------------------------------------------
Facebook integration : Slack integration + https://www.youtube.com/watch?v=tFYS6JVYNTI
required credentials : 
    verify : <bot_name>
    secret 
    page-access-token 

to run: 
    python -m rasa_core.run -d models/current/dialogue -u models/current/nlu --port 5002 --connector facebook --credentials slack_credentials.yml --endpoints endpoints.yml
