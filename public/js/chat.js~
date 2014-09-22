$(function(){

     var socket = io();
    var btnSend=$("#btnSend");
    var txtMessage= $("#txtMessage");
   var txtMsgRecord=$("#txtMsgRecord");
var txtUserName=$("#txtUserName");

function sendMessage(){
    var message=txtMessage.val();
var yiyouMsg=txtMsgRecord.val();
yiyouMsg=(yiyouMsg===""?"":(yiyouMsg+"\n"));
txtMsgRecord.val(yiyouMsg+"\t\t\t\t我说："+message);


var userName=txtUserName.val()==""?"匿名用户":txtUserName.val();
var data={message:message,userName:userName}
   socket.emit('serverMessage', data);
}

btnSend.click(function(){
sendMessage();
});

socket.on('clientMessage', function (data) {
     txtMsgRecord.val(txtMsgRecord.val()+"\n"+data.userName+"说:"+data.message);
 });

});
