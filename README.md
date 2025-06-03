# index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Find the Femur Game</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      background-color: #f0f8ff;
    }
    h1 {
      color: #2c3e50;
    }
    .skeleton-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      padding: 20px;
      justify-content: center;
    }
    .bone {
      padding: 20px;
      background: #fff;
      border: 2px solid #ccc;
      cursor: pointer;
      transition: 0.2s;
    }
    .bone:hover {
      background-color: #dff0d8;
    }
  </style>
</head>
<body>
  <h1>Find the Femur!</h1>
  <p>Click on the femur bone among these horse bones:</p>
  <div class="skeleton-grid">
    <div class="bone" onclick="checkBone(this, false)">Scapula</div>
    <div class="bone" onclick="checkBone(this, false)">Tibia</div>
    <div class="bone" onclick="checkBone(this, true)">Femur</div>
    <div class="bone" onclick="checkBone(this, false)">Humerus</div>
    <div class="bone" onclick="checkBone(this, false)">Ulna</div>
    <div class="bone" onclick="checkBone(this, false)">Radius</div>
    <div class="bone" onclick="checkBone(this, false)">Pelvis</div>
    <div class="bone" onclick="checkBone(this, false)">Metatarsal</div>
  </div>

  <script>
    function checkBone(element, isFemur) {
      if (isFemur) {
        alert("🎉 Correct! You found the femur!");
      } else {
        alert("❌ Not the femur. Try again!");
      }
    }
  </script>
</body>
</html>
