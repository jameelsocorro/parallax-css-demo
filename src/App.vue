<script setup></script>

<template>
  <main>
    <div class="parallax">
      <div class="parallax-img__layer--0" />
      <div class="parallax-img__layer--1" />
      <div class="parallax-img__layer--2" />
      <div class="parallax-img__layer--3" />
      <div class="parallax-img__layer--4" />
      <span class="montserrat parallax-title"> Eolan’s Watch </span>
      <div class="parallax-img__layer--5" />
      <div class="parallax-img__layer--6" />
      <div class="parallax-img__layer--7" />
    </div>

    <div class="content">
      <header class="content__header">
        <div class="montserrat title">A Story of Eolan</div>
        <div class="montserrat subtitle">Guardian of the Forest Mountain</div>
      </header>
      <p>
        Once upon a time, in a dense forest nestled in the heart of a towering mountain range, there
        stood a solitary watchtower. This was no ordinary watchtower. It was known as the "Eye of
        the Forest."
      </p>

      <p>
        The watchtower was built by an ancient civilization, known for their wisdom and love for
        nature. They believed that the watchtower, standing tall amidst the verdant expanse, would
        serve as a guardian of the forest.
      </p>

      <p>
        The watchtower was manned by a lone watcher named Eolan. Eolan was not just a guardian but
        also a friend to the creatures of the forest. He had a special bond with them, understanding
        their language and often helping them in times of need.
      </p>

      <p>
        One day, a great storm was brewing. Eolan, from his vantage point in the watchtower, saw the
        dark clouds gathering over the forest. He knew he had to warn the creatures of the impending
        danger.
      </p>

      <p>
        With the help of the birds, he sent out a warning to every corner of the forest. The
        animals, big and small, took shelter in their dens and nests. The storm raged on for hours,
        uprooting trees and causing havoc.
      </p>

      <p>
        When the storm finally subsided, Eolan looked out from the watchtower. The forest was in
        disarray, but there was no loss of life. The animals had heeded his warning and taken
        shelter in time.
      </p>

      <p>
        In the aftermath of the storm, Eolan, along with the creatures of the forest, worked
        tirelessly to restore the forest to its former glory. The watchtower had served its purpose,
        protecting the forest and its inhabitants.
      </p>

      <p>
        From that day forward, the watchtower was not just a structure of stone and wood, but a
        symbol of unity and resilience. And Eolan, the watcher of the tower, was revered as the
        guardian of the forest, a true friend to all its creatures.
      </p>
    </div>
  </main>
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
  overflow: hidden;
}

.parallax > * {
  grid-area: stack;
  animation: parallax linear;
  animation-timeline: scroll(root);
}

.parallax-title {
  width: 100%;
  text-align: center;
  font-size: 4rem;
  font-weight: 800;
  color: #530031;
  text-transform: uppercase;
  margin-top: -6vh;
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
  --parallax-speed: -10.5;
  height: 220vh;
  width: 100%;
  background-color: #2d112b;
  position: absolute;
  top: 80vh;
}

.content {
  position: relative;
  z-index: 10;
  background-color: #2d112b;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin: auto;
  align-items: center;
  height: 100vh;
  padding-top: 100px;
}

.content > * {
  color: #fafafa;
  text-align: justify;
  max-width: 800px;
}

.content__header {
  text-align: center;
}

.montserrat {
  font-family: 'Montserrat', sans-serif;
  letter-spacing: 0.15em;
}

.title {
  font-size: 2rem;
  font-weight: 600;
}
.subtitle {
  font-size: 1.5rem;
  font-weight: 200;
}
</style>
