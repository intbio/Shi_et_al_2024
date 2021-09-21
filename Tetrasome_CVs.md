
### Characteristic modes of tetrsome molecular dynamics (were extracted using Principal component analysis of covarience matrix for CA-atoms of histone tetramer globular part) 
[Back](http://intbio.github.io/Tetrasome_MD_2021/)

<html lang="en">
<head>
  <meta charset="utf-8">
</head>
<body>
  <p style="color:#020AED;font-size:22px;font-family:verdana;font-weight: bold;text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;display: inline">H3</p> 
  <p style="color:#009933;font-size:22px;font-family:verdana;font-weight: bold;text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;display: inline">H4</p>
  <p style="color:#808080;font-size:22px;font-family:verdana;font-weight: bold;text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;display: inline">DNA</p>
 <h3> Mode 1</h3>
  <script src="https://unpkg.com/ngl@2.0.0-dev.35/dist/ngl.js"></script>
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      var stage = new NGL.Stage("viewport0",{ backgroundColor:"#FFFFFF" });
      stage.loadFile("trj/tetr_glob.pdb").then(function (nucl) {
        var aspectRatio = 2;
        var radius = 1.5;
        nucl.addRepresentation('cartoon', {
           "sele": ":A :E", "color": 0x020AED,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":B :F", "color": "green","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":C :G", "color": 0xE0F705,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":D :H", "color": 0xCE0000,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": "nucleic", "color": "grey","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('base', {
           "sele": "nucleic", "color": "grey"});
        NGL.autoLoad("trj/tetr_cv1.xtc").then(function (frames) {
          nucl.addTrajectory(frames);
          var traj = nucl.trajList[0].trajectory;
          var player = new NGL.TrajectoryPlayer( traj,{step: 1, timeout: 20, direction : "bounce"});
          player.play();
        });  
        nucl.autoView();
      });
    });
  </script>
  <div id="viewport0" style="width:500px; height:500px; border: thin solid black"></div>
      
    
  <h3> Mode 2</h3>
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      var stage = new NGL.Stage("viewport1",{ backgroundColor:"#FFFFFF" });
      stage.loadFile("trj/tetr_glob.pdb").then(function (nucl) {
        var aspectRatio = 2;
        var radius = 1.5;
        nucl.addRepresentation('cartoon', {
           "sele": ":A :E", "color": 0x020AED,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":B :F", "color": "green","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":C :G", "color": 0xE0F705,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":D :H", "color": 0xCE0000,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": "nucleic", "color": "grey","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('base', {
           "sele": "nucleic", "color": "grey"});
        NGL.autoLoad("trj/tetr_cv2.xtc").then(function (frames) {
          nucl.addTrajectory(frames);
          var traj = nucl.trajList[0].trajectory;
          var player = new NGL.TrajectoryPlayer( traj,{step: 1, timeout: 20, direction : "bounce"});
          player.play();
        });  
        nucl.autoView();
      });
    });
  </script>
  <div id="viewport1" style="width:500px; height:500px; border: thin solid black"></div>
  
  <h3> Mode 3</h3>
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      var stage = new NGL.Stage("viewport2",{ backgroundColor:"#FFFFFF" });
      stage.loadFile("trj/tetr_glob.pdb").then(function (nucl) {
        var aspectRatio = 2;
        var radius = 1.5;
        nucl.addRepresentation('cartoon', {
           "sele": ":A :E", "color": 0x020AED,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":B :F", "color": "green","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":C :G", "color": 0xE0F705,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": ":D :H", "color": 0xCE0000,"aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('cartoon', {
           "sele": "nucleic", "color": "grey","aspectRatio":aspectRatio, "radius":radius,"radiusSegments":1,"capped":0 });
        nucl.addRepresentation('base', {
           "sele": "nucleic", "color": "grey"});
        NGL.autoLoad("trj/tetr_cv3.xtc").then(function (frames) {
          nucl.addTrajectory(frames);
          var traj = nucl.trajList[0].trajectory;
          var player = new NGL.TrajectoryPlayer( traj,{step: 1, timeout: 20, direction : "bounce"});
          player.play();
        });  
        nucl.autoView();
      });
    });
  </script>
  <div id="viewport2" style="width:500px; height:500px; border: thin solid black"></div>
</body>
</html>
