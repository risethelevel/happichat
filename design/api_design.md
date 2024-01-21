# API Chat Design
## Send a Message
* Send a message:
- Method POST 
- Endpoint https://happichat.com/v1/send
- Body: 
```json
    {
        "sender_id": "",
        "sender_ip": "",
        "sender_name": "",
        "body": "",
        "encoding_key": "",
        "attachment": "" 
    }
```
- Method POST:
- Enpoint: https://happichat.com/v1/create-multipart
- Method POST:
- Enpoint: https://happichat.com/v1/upload-part
- Method POST:
- Enpoint: https://happichat.com/v1/complete-multipart

