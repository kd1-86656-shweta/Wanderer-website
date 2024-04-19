<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Switch Popup</title>
<style>
.container {
  text-align: center;
  padding-top: 50px;
}

.popup {
  display: none;
  position: fixed;
  z-index: 1;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border: 1px solid #ccc;
  background-color: #fff;
  padding: 20px;
}

.closeBtn {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
}
</style>
</head>
<body>
<div class="container">
  <button id="toggleBtn">Toggle Popup</button>
  <div id="popup" class="popup">
    <span class="closeBtn" id="closeBtn">&times;</span>
    <p>This is a popup!</p>
  </div>
</div>
<script>
document.addEventListener('DOMContentLoaded', function() {
  const toggleBtn = document.getElementById('toggleBtn');
  const popup = document.getElementById('popup');
  const closeBtn = document.getElementById('closeBtn');

  toggleBtn.addEventListener('click', function() {
    if (popup.style.display === 'none' || popup.style.display === '') {
      popup.style.display = 'block';
    } else {
      popup.style.display = 'none';
    }
  });

  closeBtn.addEventListener('click', function() {
    popup.style.display = 'none';
  });
});
</script>
</body>
</html>