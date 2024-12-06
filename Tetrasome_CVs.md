
### Characteristic modes of tetrsome molecular dynamics 

Modes were extracted from tetrasome MD trajectory (TETR<sub>124, 2</sub>) using Principal component analysis of covarience matrix for CA-atoms of histone tetramer globular part (without flexible tails). PCA was performed via Gromacs 2020.1 program. 
This page presents first 3 tetrasome characteristic modes. Each mode was described with interpolation between the two extreme projections along a trajectory on the average structure and projection profile of a tetrasome (blue) and nucleosome (red) trajectories on this mode. 

[Back](http://intbio.github.io/Shi_et_al_2024/)

<html lang="en">
<head>
  <meta charset="utf-8">
</head>
<body>
  <p style="color:#020AED;font-size:22px;font-family:verdana;font-weight: bold;text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;display: inline">H3</p> 
  <p style="color:#009933;font-size:22px;font-family:verdana;font-weight: bold;text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;display: inline">H4</p>
 <h3> Mode 1</h3>
  Pac-man-like tetramer movement (opening); describes 29% of trajectory variance. 
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
</body>
</html>

### Tetrasome trajectory projection on the 1st mode 

![3rd](dat/1_1_vec.png)

<html lang="en">
<head>
  <meta charset="utf-8">
</head>
<body>
  <h3> Mode 2</h3>
  Torsion tetramer movement; describes 26% of trajectory variance. 
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
 
 
</body>
</html>

### Tetrasome trajectory projection on the 2nd mode 

![3rd](dat/2_1_vec.png)
  
  
<html lang="en">
<head>
  <meta charset="utf-8">
</head>
<body>
  <h3> Mode 3</h3>
  This mode escribes 10% of trajectory variance. 
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

### Tetrasome trajectory projection on the 3rd mode 

![3rd](dat/3_1_vec.png)
