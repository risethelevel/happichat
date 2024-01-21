
# API Chat Design
## Join Chat
As user we want to join the chat using a mobile user interface. During the join we want to use the keypair to get
the a private key to encrypt all the messages.

* Join a chat:
- Method POST
- Endpoint: https://happichat.com/v1/join
- Request:   
```
{
    "sender_user": "",
    "sender_password": "",
    "public_key": "",
    "hmac": ""
}
```
- Response:
```
{
    "user_id" : "",
    "session_id" : "",
    "private_key"":""
    "hmac": "",
    "key_expiration_seconds": "",
    "error_message": "",
}
```
## Send a Message
As user we want to send text messages, the messages
This section include the section
* Send a message:
- Method POST 
- Endpoint https://happichat.com/v1/send
Request  
```json
    {
        "session_id": "",
        "sender_id": "",
        "sender_ip": "",
        "sender_user": "",
        "encrypted_body": "",
        "attachment_id": "" 
    }
```
- Method POST:
- Enpoint: https://happichat.com/v1/upload-attachment

# Websocket Notification.
