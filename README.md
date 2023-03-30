# web-chat-sdk-readme
Readme File of web chat-sdk-main
# web-chat-sdk

## Web Chat SDK.
*You can use the web chat SDK to embed the web chat into your application with custom GUI.*


## Installation

### Step-1: Import the socket.io and place into your web app:

### Step-2 : Handle registration on chat server using socket with join emit event

   * Events emit when user register on socket server
   * @param { string } emailId - first name of user who has readed the message.
   * @param { string } user_id - ID of user.
   * @param { string } roomName - Room name in which message is read.
   * @param { string } short_name - short name of user who is registering on socket server.
   * @param { string } last_name - last name of user who is registering on socket server.
   * @param { string } role -  leave role blank.
   

```javascript
this.socket.emit('join', {
      emailId: "mukesh.kumar@startelelogic.co.in",
      user_id: "",
      roomName: "",
      short_name: "",
      limit: "",
      last_name: "",
      role: ""
});
```


### Step-2 : Send an event on socket with emit sendMessage event to send one to one message between customer and agent

   * @param { string } roomname
   * @param { string } message
   * @param { string } receiver
   * @param { string } time
   * @param { string } filename
   * @param { string } size
   * @param { string } team_id
   * @param { string } uuid
   * @param { string } last_replied_time
   * @param { string } replied_type
   * @param { string } replied_uuid
   * @param { string } user_id

```javascript
this.socket.emit('sendMessage', {
      roomname: "",
      message: "",
      receiver: "",
      time: "",
      filename: "",
      size: "",
      team_id: "",
      uuid: "",
      last_replied_time: "",
      replied_type: "",
      replied_uuid: "",
      user_id: ""
});
```

### Step-3 : Send an event on socket with emit receivedMessage event to send one to one message between customer and agent

   * @param { string } roomname
   * @param { string } message
   * @param { string } receiver
   * @param { string } time
   * @param { string } filename
   * @param { string } size
   * @param { string } team_id
   * @param { string } uuid
   * @param { string } last_replied_time
   * @param { string } replied_type
   * @param { string } replied_uuid
   * @param { string } user_id

```javascript
this.socket.emit('receivedMessage', {
      roomname: "",
      message: "",
      receiver: "",
      time: "",
      filename: "",
      size: "",
      team_id: "",
      uuid: "",
      last_replied_time: "",
      replied_type: "",
      replied_uuid: "",
      user_id: ""
});
```

### Step-4 : Send an event on socket with emit sendImage event to send one to one image sharing between customer and agent

   * @param { string } roomname
   * @param { string } message
   * @param { string } receiver
   * @param { string } time
   * @param { string } filename
   * @param { string } size
   * @param { string } team_id
   * @param { string } uuid
   * @param { string } last_replied_time
   * @param { string } replied_type
   * @param { string } replied_uuid
   * @param { string } user_id

```javascript
this.socket.emit('sendImage', {
      roomname: "",
      message: "",
      receiver: "",
      time: "",
      filename: "",
      size: "",
      team_id: "",
      uuid: "",
      last_replied_time: "",
      replied_type: "",
      replied_uuid: "",
      user_id: ""
});
```

### Step-5 : Send an event on socket with emit received message event to send one to one message between customer and agent

   * @param { string } roomname
   * @param { string } message
   * @param { string } receiver
   * @param { string } time
   * @param { string } filename
   * @param { string } size
   * @param { string } team_id
   * @param { string } uuid
   * @param { string } last_replied_time
   * @param { string } replied_type
   * @param { string } replied_uuid
   * @param { string } user_id

```javascript
this.socket.emit('receivedMessage', {
      roomname: "",
      message: "",
      receiver: "",
      time: "",
      filename: "",
      size: "",
      team_id: "",
      uuid: "",
      last_replied_time: "",
      replied_type: "",
      replied_uuid: "",
      user_id: ""
});
```

### Step-6 : Send an event on socket by customer with emit customer_query event to send to send request to available agents

   * @param { string } customer_name
   * @param { string } customer_mail
   * @param { string } customer_uuid
   
```javascript
this.socket.emit('customer_query', {
      customer_name: "",
      customer_mail: "",
      customer_uuid: ""
});
```

### Step-7 : Send an event on socket by customer with emit customer_query event to send to send request to available agents

   * @param { string } agent_uuid
   * @param { string } agent_email
   * @param { string } agent_name
   * @param { string } customer_email
   * @param { string } customer_uuid
   
```javascript
this.socket.emit('agent_assign', {
      agent_uuid: "",
      agent_email: "",
      agent_name: "",
      customer_email: "",
      customer_uuid: ""
});
```

### Step-2 : Show typing indicator  with typing emit event
   * @param { string } user_id - ID of user.
   
```javascript
this.socket.emit('typing', {
      user_id: ""
});
```
