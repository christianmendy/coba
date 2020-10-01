<html>
<head>
  <meta charset="UTF-8">
  <title>Enterprise Web Chat</title>
  <meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1,user-scalable=no" />
  <link rel='stylesheet prefetch' href='https://fonts.googleapis.com/css?family=Open+Sans'>
  <link rel="stylesheet" href="css/indigo.css">
  <link rel="stylesheet" href="css/widget.css">
  <link rel="stylesheet" href="css/lightslider.css">
	<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1,user-scalable=no" />
	<style type="text/css">
		html {
			background: url(images/bg-login.svg) no-repeat;
			height: 100%;
			background-size: cover;
		}
	</style>
  <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAnDdTmQAozPcMpKcPN06jD5cy0B5xt8Fw&libraries=places"></script>
  <script src="https://www.google.com/recaptcha/api.js"></script>
  <script src="http://code.responsivevoice.org/responsivevoice.js"></script>
  <script src='js/jquery-2.1.3.min.js'></script>
  <script src='js/iframeResizer.contentWindow.js'></script>
  <script src='js/iframeResizer.js'></script>
  <script src='js/lightslider.js'></script>  
  <script src='js/lazyload.min.js'></script>  
  <script src="js/cryptojs/pbkdf2.js"></script>
  <script src="js/cryptojs/aes.js"></script>
  <script src="js/cipher/aes-util.js"></script>
  <script src="js/stp.js"></script>
  <script src="js/sjs.js"></script>
  <script src="js/chat.js"></script>
  <script src="js/fuse.js"></script>
  <script src="js/speech.js"></script>
  <script>
    $(document).ready(function () {
      Chat.init({
					header: 'Selamat Datang di Jenius Help',
					login_sub_header: '',
					connect_message: 'Punya pertanyaan seputar Jenius? <br>Hubungi Jenia, yuk!',
					chat_sub_header: 'OUR AGENT WILL SERVE YOU SHORTLY',
					triggerMenu: 'main menu',
					url: 'https://apidev.btpn.com/chat/v2',
					client_id: 'f2f61c90e098e5f4ae699f6a6a66c1ba',
					client_secret: '526a49ec50be66fd4ca42cd8f70120f6',
					type_placeholder: 'Type message...',
					avatar: 'images/jenia_orange.jpg',
					icon_avatar: 'images/jenia.jpg',
					agent_avatar: 'images/jenia_orange.jpg',
					enable_attachment: true,
					enable_voice: false,
					enable_speech: false,
					enable_queue: false,
					enable_history: true,
					compatibility_mode: true,
					queue_text: "⏰NOMOR URUT: ",
					enable_campaign: true,
					campaign_avatar: 'http://www.inmotion.co.id/assets/images/logo/sri_face.png',
					campaign_title: 'Jenia',
					campaign_text: 'Hello 👋, What do you think about our pricing ?',
					campaign_timer: 5000,
					campaign_menu: [{"label":"Promotion", "value":"Layanan", "icon":"https://i.pinimg.com/originals/1b/1e/37/1b1e37721cf248b07ae7ed07966df60b.gif"}, {"label":"Product", "value":"Produk", "icon":"https://cdn.dribbble.com/users/128315/screenshots/2605603/ridebot2.gif"}, {"label":"Live Agent", "value":"Sambungkan ke cs", "icon":"https://media2.giphy.com/media/o9uoQFxayuxs4/giphy.gif"}],
					max_upload_message: "File size limit exceeded. Maximum filesize is [max_filesize]"
				});
	});
	
	function emulateMessage(count) {
		for (var i=0;i<count;i++) {
			var msgObj = {message: "", messageHash: "", token: "", transactionId: ""}
			msgObj.message = "Hai";
			msgObj.messageHash = fuse(msgObj.messageHash);
			msgObj.token = Chat.token;
			msgObj.transactionId = "" + getTimeInMillliseconds();
			sendTextMessage(msgObj, msgObj.message);
		}
	}
  </script>
</head>
<body>  
	<button onclick="emulateMessage(50);return false;">Emulate 50 Messages</button><br/>
</body>
</html>
