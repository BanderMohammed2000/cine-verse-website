<template>
  <div>
    <svg class="container" viewBox="0 0 40 40" height="40" width="40">
      <circle
        class="track"
        cx="20"
        cy="20"
        r="17.5"
        pathlength="100"
        stroke-width="5px"
        fill="none"
      />
      <circle
        class="car"
        cx="20"
        cy="20"
        r="17.5"
        pathlength="100"
        stroke-width="5px"
        fill="none"
      />
    </svg>
  </div>
</template>

<style scoped>
.container {
  --uib-size: 100px;
  --uib-color: var(--main-color);
  --uib-speed: 0.8s;
  --uib-bg-opacity: 0.1;
  height: var(--uib-size);
  width: var(--uib-size);
  transform-origin: center;
  animation: rotate var(--uib-speed) linear infinite;
  will-change: transform;
  overflow: visible;
}

.car {
  fill: none;
  stroke: var(--uib-color);
  stroke-dasharray: 25, 75;
  stroke-dashoffset: 0;
  stroke-linecap: round;
  transition: stroke 0.5s ease;
}

.track {
  fill: none;
  stroke: var(--uib-color);
  opacity: var(--uib-bg-opacity);
  transition: stroke 0.5s ease;
}

@keyframes rotate {
  100% {
    transform: rotate(360deg);
  }
}
</style>
