<template>
  <div class="fullscreen body text-white text-center q-pa-md flex flex-center">
    <div>

      <div class="text-h2" style="opacity:.4">
        This page will be available soon:D
      </div>

      <q-btn
        class="q-mt-xl"
        color="white"
        text-color="blue"
        unelevated
        to="/"
        label="Go Home"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ErrorNotFound'
})
</script>

<style>
.body {
	background: linear-gradient(50deg, #00071d, #2c3d52, #040031, #1c2646);
	background-size: 400% 400%;
	animation: gradient 9s ease infinite;
	height: 100vh;
}

@keyframes gradient {
	0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}</style>
