# real-time-chat-application
A real-time chat application built using React, Node.js, Express, Socket.io, and MongoDB for instant messaging and user communication.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chat Application</title>

<style>
body{
    font-family:Arial,sans-serif;
    background:#f4f4f4;
}

.container{
    width:400px;
    margin:50px auto;
    background:white;
    padding:20px;
    border-radius:10px;
    box-shadow:0 0 10px rgba(0,0,0,0.2);
}

h2{
    text-align:center;
}

#chatBox{
    height:300px;
    border:1px solid #ddd;
    overflow-y:auto;
    padding:10px;
    margin-bottom:10px;
}

.message{
    background:#007bff;
    color:white;
    padding:8px;
    margin:5px 0;
    border-radius:5px;
}

input{
    width:75%;
    padding:10px;
}

button{
    padding:10px;
    background:#28a745;
    color:white;
    border:none;
    cursor:pointer;
}
</style>
</head>

<body>

<div class="container">

<h2>Chat Application</h2>

<div id="chatBox"></div>

<input type="text" id="message" placeholder="Type a message">

<button onclick="sendMessage()">Send</button>

</div>

<script>

function sendMessage(){

    let input =
    document.getElementById("message");

    let text = input.value.trim();

    if(text === "") return;

    let msg =
    document.createElement("div");

    msg.className = "message";
    msg.innerText = text;

    document
    .getElementById("chatBox")
    .appendChild(msg);

    input.value = "";

    document
    .getElementById("chatBox")
    .scrollTop =
    document
    .getElementById("chatBox")
    .scrollHeight;
}

</script>

</body>
</html>
