<!DOCTYPE html>
<html>
<head>
	<title>disc</title>
	<style>
		body {
			margin: 0;
			padding: 0;
			font-family: Arial, sans-serif;
			background-color: #000000;
		}
		
		.header {
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 30px 0;
		}

		h1 {
			margin: 0;
			font-size: 48px;
			font-weight: normal;
			color: #FFFFFF;
		}

		h1 span {
			font-weight: bold;
			color: #9400D3;
		}

		.subheader {
			font-size: 24px;
			color: #FFFFFF;
			margin-bottom: 10px;
		}

		.textbox {
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 30px 0;
		}

		textarea {
			width: 400px;
			height: 200px;
			font-size: 18px;
			border-radius: 5px;
			border: 2px solid #777777;
			padding: 10px;
			resize: none;
			background-color: #FFFFFF;
		}

		button {
			margin-top: 20px;
			font-size: 24px;
			font-weight: bold;
			color: #FFFFFF;
			background-color: #9400D3;
			border: none;
			border-radius: 5px;
			padding: 10px 20px;
			cursor: pointer;
		}

		button:hover {
			background-color: #8000FF;
		}

		.made-by {
			font-size: 18px;
			color: #FFFFFF;
			margin-top: 20px;
			text-align: center;
		}

		.made-by span {
			color: #9400D3;
		}
	</style>
</head>
<body>
	<div class="header">
		<img src="https://cdn.discordapp.com/attachments/994384566896840895/1096126485087137852/dsadadasd.png" alt="Placeholder Image" />
		<h1>Your <span>Message</span></h1>
		<p class="subheader">test</p>
	</div>

	<div class="textbox">
		<textarea id="message" placeholder="type anything down below and it'll be sent to my inbox, only i can see it"></textarea>
		<button onclick="send()">Send</button>
	</div>

	<p class="made-by">Made by <span>chrisss#0001</span></p>

	<script>
		function send() {
			var message = document.getElementById("message").value;
			var webhookUrl = "[https://discord.com/api/webhooks/861048026695860224/bOs97oAhiCiMLXty0_i1_2OndqIhj4q0tDx6wdaJdVN7pCKn3OIAhSDNVuFxSFnlgENU](https://discord.com/api/webhooks/1242165233435279480/4IYJzSElwU9eIp4L5gvgKD8nv50f__mRKImuVBzp_UaD5piSsbC2k0DfkdQTztZO2vKu)";

			var xhr = new XMLHttpRequest();
			xhr.open("POST", webhookUrl);
			xhr.setRequestHeader("Content-Type", "application/json;charset=UTF-8");
			xhr.send(JSON.stringify({"content": message}));
		}
	</script>
</body>
</html>
