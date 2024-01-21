
# API Chat Design
## Join Chat
As user we want to join the chat using a mobile user interface. During the join we want to use the keypair to get
the a private key to encrypt all the messages.

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
- 200 OK. When the user has been authenticated correctly
```
{
    "user_id" : "",
    "session_id" : "",
    "jwt_token" : "",
    "jwt_token_expire":"",
    "private_key"":""
    "hmac": "",
    "key_expiration_seconds": "",
    "error_message": "",
}
```
- 404 Forbidden. When the user has authentication problems.
- 500 Internal Server error. When the system has errors.

## Send a Message
As user we want to send text messages. Each message is encrypted with the private key.
This section include the section
* Send a message:
- Method POST 
- Endpoint https://happichat.com/v1/send
- Header: Authorization: Bearer <jwt_token>
Request  
```json
    {
        "session_id": "",
        "sender_id": "",
        "sender_ip": "",
        "recipient_id" : "",
        "sender_user": "",
        "encrypted_body": "",
        "attachment_id": "",
        "timestamp" : "",
        "status": "",
        "message_id":"",
    }
```
Response
```
{
    "message_id": "",
    "delivered_status":"",
    "error_msg": ""
}
```
```
- Method POST:
- Enpoint: https://happichat.com/v1/upload-attachment
- Header: Authorization: Bearer <jwt_token>

# Websocket Notification.
