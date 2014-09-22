var alluser=[];
function startChatServer(server){
	var io = require('socket.io')(server);
	io.on('connection', function(socket){ 
	console.log("有用户请求我们的聊天服务器");
	socket.on('serverMessage', function (data) {
	console.log(JSON.stringify(data));
	    socket.broadcast.emit('clientMessage', data);
	 });
	});
}
module.exports=startChatServer;


