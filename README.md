<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Run Face Instagram</title>

<style>
body{
  margin:0;
  height:100vh;
  background:#111;
  overflow:hidden;
  font-family:Arial;
}

/* 😄 الوجه */
.face{
  width:120px;
  height:120px;
  background:#fff;
  border-radius:50%;
  position:absolute;
  top:40%;
  left:40%;
  transition:0.2s;
  cursor:pointer;
  box-shadow:0 0 20px rgba(255,255,255,0.3);
}

/* عيون */
.eye{
  width:12px;
  height:20px;
  background:#000;
  border-radius:50%;
  position:absolute;
  top:35px;
}

.eye.left{ left:30px; }
.eye.right{ right:30px; }

/* فم */
.mouth{
  width:40px;
  height:20px;
  border:4px solid #000;
  border-top:none;
  border-radius:0 0 30px 30px;
  position:absolute;
  bottom:25px;
  left:50%;
  transform:translateX(-50%);
}

/* Instagram */
#igBtn{
  display:none;
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  padding:12px 18px;
  background:linear-gradient(45deg,#f58529,#dd2a7b,#8134af);
  color:white;
  text-decoration:none;
  border-radius:12px;
  font-weight:bold;
}
</style>
</head>

<body>

<div class="face" id="face">
  <div class="eye left"></div>
  <div class="eye right"></div>
  <div class="mouth"></div>
</div>

<a id="igBtn" href="https://instagram.com/red__rabbit01" target="_blank">
^_- Instagram ^_-
</a>

<script>
let face = document.getElementById("face");
let igBtn = document.getElementById("igBtn");

function moveFace(){
  let x = Math.random() * (window.innerWidth - 120);
  let y = Math.random() * (window.innerHeight - 120);

  face.style.left = x + "px";
  face.style.top = y + "px";
}

/* يهرب ملي تقرب عليه */
document.addEventListener("mousemove", moveFace);

/* ملي تضغط عليه */
face.onclick = function(){
  face.style.display = "none";
  igBtn.style.display = "block";
};
</script>

</body>
</html>
