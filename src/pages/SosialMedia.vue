<template>
    <q-layout class="flex flex-center q-pa-md body">
        <q-card class="card q-pa-md">
            <div class="flex flex-center q-mb-sm">
            <q-img class="" style="width:80px;" src="images/ava.png" />
        </div>
<div class="flex flex-center q-gutter-md row text-white">
            <q-btn class="sosmed col-12" @click="Instagram">
                    <q-avatar>
                        <i class="bi bi-instagram"></i>
                    </q-avatar>
                    <div class="fontsoc">Instagram</div>
            </q-btn>

            <q-btn class="sosmed col-12" @click="Youtube">
                    <q-avatar>
                        <i class="bi bi-youtube"></i>
                    </q-avatar>
                    <div class="fontsoc">Youtube</div>
            </q-btn>

            <q-btn class="sosmed col-12" @click="Github">
                    <q-avatar>
                        <i class="bi bi-github"></i>
                    </q-avatar>
                    <div class="fontsoc">Github</div>
            </q-btn>

            <q-btn class="sosmed col-12" @click="Linkedin">
                    <q-avatar>
                        <i class="bi bi-linkedin"></i>
                    </q-avatar>
                    <div class="fontsoc">Linkedin</div>
            </q-btn>
            
            <!-- <q-btn class="sosmed col-12" @click="Email">
                    <q-avatar>
                        <i class="bi bi-mail"></i>
                    </q-avatar>
                    <div class="fontsoc">Email</div>
            </q-btn> -->
        </div>
        </q-card>
    </q-layout>
</template>

<script>
export default {
    methods: {
  Instagram() {
      // Ganti URL berikut dengan URL profil Instagram yang ingin Anda tuju
      const instagramURL = "https://www.instagram.com/iamalparsyy";
      window.location.href = instagramURL;
    },
  Youtube() {
      // Ganti URL berikut dengan URL profil Instagram yang ingin Anda tuju
      const instagramURL = "https://www.youtube.com/channel/UCVwxMMbAjaD5qadQweX2-jQ";
      window.location.href = instagramURL;
    },
  Github() {
      // Ganti URL berikut dengan URL profil Instagram yang ingin Anda tuju
      const instagramURL = "https://github.com/arsy25";
      window.location.href = instagramURL;
    },
  Linkedin() {
      // Ganti URL berikut dengan URL profil Instagram yang ingin Anda tuju
      const instagramURL = "https://id.linkedin.com/in/muhammad-ilham-alparsy-a0a539290";
      window.location.href = instagramURL;
    },
}
}

</script>

<style>
.sosmed {
    border-radius: 20px 7px;
}

.fontsoc {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif
}

.card {
    border-radius: 10px;
    background-color: transparent;
    backdrop-filter: blur(100);
}
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