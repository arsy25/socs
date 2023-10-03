<template>
  <q-layout view="lHh Lpr lFf" class="bglay">
<div v-if="$q.platform.is.mobile">
    <q-card outlined class="navbarmenu">
      <!--ini toolbarnya-->
      <div class="row q-pa-md flex flex-center textmenu">
        <q-img class="" style="width:40px;" src="images/logo.png" />
        <q-space />
       
        <q-space></q-space>
        <q-icon
          class="flex flex-center"
          name="menu"
          v-for="size in ['md']"
          :key="size"
          :size="size"
          @click="drawer = !drawer"
        >
          <q-tooltip
            class="bg-black text-cyan-7 flex flex-center"
            transition-show="rotate"
            style="width: 100px"
            transition-hide="rotate"
            >MENU LAINNYA</q-tooltip
          >
        </q-icon>
      </div>
    </q-card>

    <q-drawer
      v-model="drawer"
      :mini="miniState"
      @mouseover="miniState = false"
      @mouseout="miniState = true"
      mini-to-overlay
      :width="250"
      :breakpoint="500"
      class="menulogo"
    >
      <q-list class="q-pa-md q-gutter-md">
        <q-item>
          <q-item-section avatar>
            <q-icon
              name="double_arrow"
              class="logo"
              v-for="size in ['md']"
              :key="size"
              :size="size"
            />
          </q-item-section>
        </q-item>
        <q-item
          to="/"
          clickable
          v-ripple
          class="menulink element1 shadow-10"
        >
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>Home</q-item-section>
        </q-item>

        <q-item
          to="/sosmed"
          clickable
          class="element2 menulink shadow-10"
        >
          <q-item-section avatar>
            <q-icon name="people" />
          </q-item-section>
          <q-item-section> Social Media </q-item-section>
        </q-item>

        <q-item to="/docs" clickable  class="element1 menulink shadow-10">
          <q-item-section avatar>
            <q-icon name="history" />
          </q-item-section>
          <q-item-section> Documentation </q-item-section>
        </q-item>

        <q-item to="/about" clickable  class="menulink element2 shadow-10">
          <q-item-section avatar>
            <q-icon name="info" />
          </q-item-section>
          <q-item-section> About </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
    </div>

<div v-else class="flex flex-center text-white"> Desktop version will be available soon
    <!-- <q-card outlined class="navbarmenu">
      <div class="row q-pa-md flex flex-center textmenu">
        <div class="col-1"></div>
        <div class="col-3 flex flex-center">
          <q-btn
            rounded
            flat
            style="width: 200px"
            class="btn"
            label="Home"
            :to="{ name: 'home' }"
          >
            <q-tooltip
              class="text-cyan-3 bg-black flex flex-center"
              transition-show="rotate"
              style="width: 100px"
              transition-hide="rotate"
              >Artikel Utama</q-tooltip
            ></q-btn
          >
        </div>
        <div class="col-3 flex flex-center">
          <q-btn
            rounded
            flat
            style="width: 200px"
            class="btn"
            label="Artikel lainnya"
            :to="{ name: 'artikellain' }"
            ><q-tooltip
              class="text-cyan-3 bg-black text-center"
              transition-show="rotate"
              style="width: 100px"
              transition-hide="rotate"
              >Klik untuk lihat artikel lain</q-tooltip
            ></q-btn
          >
        </div>
        <div class="col-3 flex flex-center">
          <q-btn
            rounded
            flat
            style="width: 200px"
            class="btn"
            label="Buat Artikel"
            :to="{ name: 'buatartikel' }"
          >
            <q-icon name="add" />
            <q-tooltip
              class="text-cyan-3 bg-black text-center"
              transition-show="rotate"
              style="width: 100px"
              transition-hide="rotate"
              >Mau buat artikel? Klik disini
            </q-tooltip>
          </q-btn>
        </div>
        <q-space></q-space>
        <q-separator color="blue" vertical />
        <q-space></q-space>
        <q-icon
          class="flex flex-center"
          name="menu"
          v-for="size in ['md']"
          :key="size"
          :size="size"
          @click="drawer = !drawer"
        >
          <q-tooltip
            class="bg-grey-8 flex flex-center"
            transition-show="rotate"
            style="width: 100px"
            transition-hide="rotate"
            >MENU LAINNYA</q-tooltip
          >
        </q-icon>
      </div>
    </q-card>

    <q-drawer
      v-model="drawer"
      :mini="miniState"
      @mouseover="miniState = false"
      @mouseout="miniState = true"
      mini-to-overlay
      :width="250"
      :breakpoint="500"
      class="menulogo"
    >
      <q-list class="q-pa-md q-gutter-md">
        <q-item>
          <q-item-section avatar>
            <q-icon
              name="double_arrow"
              class="logo"
              v-for="size in ['md']"
              :key="size"
              :size="size"
            />
          </q-item-section>
        </q-item>
        <q-item
          :to="{ name: 'home' }"
          clickable
          v-ripple
          class="menulink element1 shadow-10"
        >
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>Home</q-item-section>
        </q-item>

        <q-item
          :to="{ name: 'qna' }"
          clickable
          v-ripple
          class="element2 menulink shadow-10"
        >
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section> QNA </q-item-section>
        </q-item>

        <q-item clickable v-ripple class="element1 menulink shadow-10">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section> Inbox </q-item-section>
        </q-item>

        <q-item clickable v-ripple class="menulink element2 shadow-10">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section> Inbox </q-item-section>
        </q-item>
        <q-separator class="bg-cyan-4" />
      </q-list>
    </q-drawer> -->
    </div>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import "bootstrap-icons/font/bootstrap-icons.css";

export default {
  name: "MainLayout",
  components: {},
  data() {
    return {
      drawer: false,
      miniState: true,
    };
  },
};
</script>
<style>
:root {
  font-size: 20px;
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  --text-primary: #131111;
  --text-secondary: #ffffff;
  --text-menu: #91c8e4;
  --bg-primary: #23232e;
  --bg-secondary: #07191d;
  --transition-speed: 700ms;
  --transition-speed2: 200ms;
}
.bglay {
  background: #000000;
}

.navbartop {
  background: #000000;
  background-size: 100%;
}
.navbarmenu {
  background: #000000;
}
.textmenu {
  color: var(--text-menu);
  font-family: sans-serif;
}
.btn {
  border-radius: 20px 5px;
  background: transparent;
  transition: var(--transition-speed);
}
.btn:hover {
  filter: grayscale(0%) opacity(1);
  font-weight: 600;
  background: #69d2e7;
  color: #000000;
}
.element1 {
  border-radius: 5px 20px 5px;
  background: #69d2e7;
}
.element2 {
  border-radius: 20px 5px;
  background: #69d2e7;
}

.logo {
  transform: rotate(0deg);
  transition: transform var(--transition-speed2);
  color: #69d2e7;
}
.menulogo {
  background: #000000;
}
.menulogo:hover .logo {
  transform: rotate(-180deg);
}

.menulink {
  align-items: center;
  height: 4rem;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 500;
  color: var(--text-primary);
  filter: grayscale(5%) opacity(1);
  transition: var(--transition-speed);
}
.menulink:hover {
  filter: grayscale(0%) opacity(1);
  background: var(--bg-secondary);
  color: var(--text-secondary);
  transition: var(--transition-speed2);
  font-weight: 900;
}
</style>
