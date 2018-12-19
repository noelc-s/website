---
layout:     post
title:      Mission Trails Regional Park
subtitle:   5 Peaks 
author:     Noel Csomay-Shanklin
tags: 		  Hobbies Hiking
category:   hiking
---
<!-- Start Writing Below in Markdown -->

<iframe src='https://www.gaiagps.com/public/c6OkPlwHDqb7LSehAYKhfjzb?embed=True' style='border:none; overflow-y: hidden; background-color:white; min-width: 320px; max-width:1170px; width:100%; height: 420px;' scrolling='no' seamless='seamless'></iframe>

<button onclick="STL()">Show 3D Terrain Model</button>

<div id="STL" align="center">
<script src="https://embed.github.com/view/3d/noelc-s/website/gh-pages/stl/missionTrails.stl"></script>
</div>

<button onclick="Path()">Show 3D Path</button>

<div id="Path" align="center">
<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/dist/pa-embed-player.min.js" async></script>
<div class="pa-embed-player" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/RctJz5NY2vHUfPwMA"
  data-title="Mission Trails Loop"
  data-description="New photo · Album by Noel C-S">
  <img data-src="https://lh3.googleusercontent.com/FDNhpSn4CwxtrXZ0U07ooe4tw4DtrFUEzcG-wNlMWNWjfJLZ1sghjhgroOJpQD8HAS1GLXSsn1SHNhhYRcmTecAT04OmQnu8IqhK6EWB2sSSDuNCDFo8x2pkQsF9t2nTHd_WC2DALec=w1920-h1080" src="" alt="" />
</div>

</div>


<script>
document.getElementById("STL").style.display = "none"; 
document.getElementById("Path").style.display = "none"; 
function Path() {
  var x = document.getElementById("Path");
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
function STL() {
  var x = document.getElementById("STL");
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
</script>

