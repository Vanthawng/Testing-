# Testing-
Testing group test
<!DOCTYPE html>
<html>
    <head>
        <title>Firebase Group Chat</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
        <script src="https://www.gstatic.com/firebasejs/4.6.2/firebase.js"></script>
        <script src="https://www.gstatic.com/firebasejs/4.6.2/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/4.6.2/firebase-auth.js"></script> 
<script src="https://www.gstatic.com/firebasejs/4.6.2/firebase-database.js"></script>
        <script src="https://www.gstatic.com/firebasejs/4.6.2/firebase-firestore.js"></script>
<script src="https://www.gstatic.com/firebasejs/4.6.2/firebase-messaging.js"></script>
<script type="text/javascript">
alert("Thanks for checkout😁\nGood Advice are welcomed\n 🙏🙏Thanks Thomas🙏");
alert("Humbly request:-\nDon't create dirty spam");
var config = {
    apiKey: "AIzaSyBeaZsv8BasCPGVVIE0BF4Fos9S6JorIv4",
    authDomain: "funweb210.firebaseapp.com",
    databaseURL: "https://funweb210.firebaseio.com",
    projectId: "funweb210",
    storageBucket: "funweb210.appspot.com",
    messagingSenderId: "19664987666"
  };
  firebase.initializeApp(config);
  var grn=prompt("😀Enter Your Group Name\n'or' 😎Create Your Own Group","sololearn");
  var group="/chat/"+grn;
var database = firebase.database();
var nddl = 2 ;
var ref = firebase.database().ref(group
);
function send() {
if (nickname.value!="" && txt.value!="")
 {
var msg = "<div class=\"chatbox\"><span>"+ nickname.value.split("<").join("&lt") + ":</span><br />" + txt.value.split("<").join("&lt") + "</div>" ;
document.getElementById("txt").value = "" ;
document.getElementById("nickname").style.display = "none" ; 
firebase.database().ref(group).push({ message: msg }).key;}}ref.on("child_added" , function(data) {
var dmsg = data.val();
tabl.innerHTML =dmsg.message+document.getElementById("tabl").innerHTML}, 
function(error) 
{
alert(error.code)
});
</script>
<style type="text/css">
body {
    background:url("https://picsum.photos/400/800/?random");
    color:white;
}

#wrapper {
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    overflow: hidden;
    position: absolute;
}
input {
    border-radius:25px;
    height:50px;
    border: 2px solid white;
    width:80vw;
    max-width: 100%;
    font-size:24px;
    outline: none;
    color: white;
    padding: 0 5px;
    background-color: #ffbb00;
}

#table {
    
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 50px;
    background:transparent;
    overflow: hidden;
}
#tabl {
    height:100%;
    width:100%;
    font-weight:200;
    overflow-y:auto;
    overflow-x: hidden;
    
}
#sendbtn{
    position:absolute;
    right:0;
    bottom:0;
    border-radius:50%;
    height:60px;
    width:60px;
    border: none;
    color: white;
    font-weight: bold;
    font-size: 40px;
    outline: none;
    background-color:#7cbb00;
}
.chatbox {
    margin:15px;
    padding:5px;
    color: white;
    font-size:20px;
    background-color:rgba(255,178,0,0.5);
    max-width:85%;
    border-radius:0 30px 20px 20px;
    font-family:verdana;
}
span{
color:#f65314;
font-size:22px;
font-family:times new roman;
font-weight:bold;
}
#form {
    width: 100vw;
    position: absolute;
    bottom: 0;
}
</style> 
    </head>
    <body>
    <div id="wrapper">
    
    <div id="account">
        <div id="table">
            <div id="tabl"></div>
        </div>
        
        <div id="form">
        <input id="nickname" placeholder="Enter your Nick Name.." type="text">
        <input id="txt" maxlength="70" placeholder="Type your Message..." type="text">
        <button onclick="send()" id="sendbtn">&#10147;</button>
        </div>
    </div>
    
    </div>
    </body>
</html>
