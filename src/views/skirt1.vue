<template>
    <div>
        

<div class="container">
  <img src="../assets/skirt1-1.jpg" alt="Avatar" class="image">
  <div class="overlay">
    <div class="text">
<img src="../assets/uniqlo.png" style="width:50%; hight:100%;">
    </div>
  </div>
</div>
</div>


</template>
<style>
.container {
  position: relative;
  width: 50%;
}

.image {
  display: block;
  width: 50%;
  height: auto;
}

.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 50%;
  opacity: 0;
  transition: .5s ease;
}

.container:hover .overlay {
  opacity: 1;
}

.text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}
</style>