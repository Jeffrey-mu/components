
<template>
  <div class="container">
    <div class="shifting-card">
      <div class="content">
        <h3>Card</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti repellat, consequuntur doloribus voluptate
          esse iure?</p>
      </div>
    </div>
    <Render :code="code"/>
  </div>
</template>
<style>
.container {
  display: flex;
  padding: 24px;
  justify-content: center;
  align-items: center;
  background: #f3f1fe;
}

.shifting-card {
  width: 350px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  margin: 0.5rem;
  transition: transform 0.2s ease-out;
  box-shadow: 0 0 5px -2px rgba(0, 0, 0, 0.1);
}

.shifting-card .content {
  text-align: center;
  margin: 2rem;
  line-height: 1.5;
  color: #101010;
}
</style>
<script setup>
const code = `window.addEventListener('load', function() {
      console.log(1)
      const card = document.querySelector('.shifting-card');
const { x, y, width, height } = card.getBoundingClientRect();
const cx = x + width / 2;
const cy = y + height / 2;

const handleMove = e => {
  const { pageX, pageY } = e;
  const dx = (cx - pageX) / (width / 2);
  const dy = (cy - pageY) / (height / 2);
  e.target.style.transform =
    \`rotateX(\${ 10 * dy * -1 }deg) rotateY(\${ 10 * dx }deg)\`;
};

const handleOut = e => {
  e.target.style.transform = 'initial';
};

card.addEventListener('mousemove', handleMove);
card.addEventListener('mouseout', handleOut);
    })`
</script>
