var wordsList = [];

function init() {
  // Load the words from the dictionary text file to wordsList
  var wordsFile = "https://raw.githubusercontent.com/GirlsFirst/SIP-2017/master/Unit2_Applications/dictionary-attack/dictionary.txt?token=ADcVhZjRMd86ZdhPE2jVvIaJdQdzLA6Yks5YvvVSwA%3D%3D";
  $.get(wordsFile, function(data) {
    document.getElementById("btnSubmit").disabled = true; 
    wordsList = data.split('\n');
    document.getElementById("btnSubmit").disabled = false; 
  });
}

window.onload = init;

/* ADD YOUR CODE BELOW */

function checkPassword() {

}

<html>
  <head>
    <title>Dictionary Attack Detector</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <link rel='shortcut icon' type='image/x-icon' href='favicon.ico' />
    <link href="dictionary-attack.css" rel="stylesheet" />
    <script src="dictionary-attack.js" type="text/javascript"></script>
  </head>
  <body>
    <div>
      <h1>Dictionary Attack Detector</h1>
      <div class="content">
        <p>See if a dictionary attack can find your password!</p>
        <input id="pw"/>
        <button id="btnSubmit" onclick="checkPassword()">Check this password</button>
        <p id="results"></p>
      </div>
    </div>
  </body>
</html>
