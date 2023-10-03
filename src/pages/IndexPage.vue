<template>
  <q-page class="flex flex-center body">
<div class="text-white text-h5">Hi Everyone!
  <div>Tbh i don't know, how should i show</div>
</div>

  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
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
}

</style>
