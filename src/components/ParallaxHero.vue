<template>
  <div class="parallax">
    <div class="parallax-img__layer--0" />
    <div class="parallax-img__layer--1" />
    <div class="parallax-img__layer--2" />
    <div class="parallax-img__layer--3" />
    <div class="parallax-img__layer--4" />
    <div class="parallax-img__layer--5" />
    <div class="parallax-img__layer--6" />
    <div class="parallax-img__layer--7" />
  </div>
  <div class="content"></div>
</template>

<style>
@keyframes parallax {
  to {
    transform: translateY(calc(var(--parallax-speed) * 200px));
  }
}

.parallax {
  min-height: 80vh;
  display: grid;
  grid-template-areas: 'stack';
  padding-top: 30vh;
}

.parallax > * {
  grid-area: stack;
  animation: parallax linear;
  animation-timeline: scroll(root);
}

.parallax-img__layer--0 {
  --parallax-speed: 10;
  background: url('/src/assets/images/layer_0.png') no-repeat center center / cover;
}

.parallax-img__layer--1 {
  --parallax-speed: 7;
  background: url('/src/assets/images/layer_1.png') no-repeat center center / cover;
}

.parallax-img__layer--2 {
  --parallax-speed: 5;
  background: url('/src/assets/images/layer_2.png') no-repeat center center / cover;
}

.parallax-img__layer--3 {
  --parallax-speed: 3;
  background: url('/src/assets/images/layer_3.png') no-repeat center center / cover;
}

.parallax-img__layer--4 {
  --parallax-speed: -3;
  background: url('/src/assets/images/layer_4.png') no-repeat center center / cover;
}

.parallax-img__layer--5 {
  --parallax-speed: -5;
  background: url('/src/assets/images/layer_5.png') no-repeat center center / cover;
}

.parallax-img__layer--6 {
  --parallax-speed: -10;
  background: url('/src/assets/images/layer_6.png') no-repeat center center / cover;
}

.parallax-img__layer--7 {
  --parallax-speed: -10;
  height: 40vh;
  width: 100%;
  background-color: #2d112b;
  position: absolute;
  top: 80vh;
}

.parallax-header {
}
.parallax-header__inner {
}
</style>
