<center><font face="Arial" size="6">マルバツゲーム<br><br><head>
<style>
.cell{width:50px; height:50px; font-size:30pt;}
</style>
</head>
<script type="text/javascript" language="JavaScript">
var count=0;
function clickA(z)
{
if(z.innerText != ""){
alert("クリックできません");
return;
}
if(count++ %2 == 0){z.innerText = "○";}
else {z.innerText = "×";}

var ret = judge();
if(ret){alert(ret);}
}

function judge()
{
var b0 = document.getElementById("b0").innerText;
var b1 = document.getElementById("b1").innerText;
var b2 = document.getElementById("b2").innerText;
var b3 = document.getElementById("b3").innerText;
var b4 = document.getElementById("b4").innerText;
var b5 = document.getElementById("b5").innerText;
var b6 = document.getElementById("b6").innerText;
var b7 = document.getElementById("b7").innerText;
var b8 = document.getElementById("b8").innerText;

if(b0 == b1 && b1 == b2 && b0 != "" )
{winner = b0;}
else if (b3 == b4 && b4 == b5 && b3 != "" )
{winner = b3;}
else if (b6 == b7 && b7 == b8 && b7 != "" )
{winner = b6;}
else if (b0 == b3 && b3 == b6 && b0 != "" ) 
{winner = b0;}
else if (b1 == b4 && b4 == b7 && b1 != "" )
{winner = b1;}
else if (b2 == b5 && b5 == b8 && b2 != "" )
{winner = b2;}
else if (b0 == b4 && b4 == b8 && b0 != "" )
{winner = b0;}
else if (b2 == b4 && b4 == b6 && b2 != "" )
{winner = b2;}
if (winner) {var str = winner + "の勝ち";}
else if (count == 9) {引き分け;} 
return str ;;
}
</script>
<body>
<table border="4">
<caption>○×ゲーム</caption>
<tr>
<td class="cell" id="b0" onclick="clickA(this);"> </td>
<td class="cell" id="b1" onclick="clickA(this);"> </td>
<td class="cell" id="b2" onclick="clickA(this);"> </td>
</tr>
<tr>
<td class="cell" id="b3" onclick="clickA(this);" ></td>
<td class="cell" id="b4" onclick="clickA(this);"> </td>
<td class="cell" id="b5" onclick="clickA(this);"> </td>
</tr>
<tr>
<td class="cell" id="b6" onclick="clickA(this);"> </td>
<td class="cell" id="b7" onclick="clickA(this);"> </td>
<td class="cell" id="b8" onclick="clickA(this);"> </td>
</tr>
</table>
<input type="reset" onclick="location.reload();">
<script type="module">
  // Import the functions you need from the SDKs you need
  import { initializeApp } from "https://www.gstatic.com/firebasejs/9.6.5/firebase-app.js";
  import { getAnalytics } from "https://www.gstatic.com/firebasejs/9.6.5/firebase-analytics.js";
  // TODO: Add SDKs for Firebase products that you want to use
  // https://firebase.google.com/docs/web/setup#available-libraries

  // Your web app's Firebase configuration
  // For Firebase JS SDK v7.20.0 and later, measurementId is optional
  const firebaseConfig = {
    apiKey: "AIzaSyDdhB3d_OC1gIC6kpJBrs4pDGRWXIoWoEA",
    authDomain: "test-a2b9b.firebaseapp.com",
    projectId: "test-a2b9b",
    storageBucket: "test-a2b9b.appspot.com",
    messagingSenderId: "342542475097",
    appId: "1:342542475097:web:306cfd2c3718bf66217648",
    measurementId: "G-42PTFZF742"
  };

  // Initialize Firebase
  const app = initializeApp(firebaseConfig);
  const analytics = getAnalytics(app);
</script><br><br><a href="javascript:history.back()"><img src="btn01-11.png"></a>
