<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/AppHeader.vue'
</script>

<template>
  <div id="socializer-app">
        <div class="app__container">
            <!-- <nav class="app__menu">
                <the-menu />
            </nav> -->

            <header class="app__header">
              <TheHeader />
            </header>

            <div class="app__content">
                <main class="app__pages">
                    <router-view />
                </main>

                <footer class="app__footer">
                    <the-footer />
                </footer>
            </div>
        </div>

        <div class="app__loading">
            <loader v-show="loadingCount" />
        </div>
    </div>

    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

        <!-- <div class="wrapper">
        <HelloWorld msg="You did it!" />

        
        </div> -->
        <!-- <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
        </nav> -->

    <!-- <RouterView /> -->
</template>

<style lang="scss">

#socializer-app {
        .app {
            &__container {
                display: grid;
                grid-template-columns: auto 1fr; // 2 columns
                // grid-template-rows: $spacing-header-height auto; // 2 rows
                height: 100vh;
                width: 100%;
            }

            &__menu {
                grid-area: 1 / 1 / 3 / 2; // row start / column start / row end / column end
            }

            &__content {
                overflow: auto;
            }
        }
    }


header {
    /* line-height: 1.5;
    max-height: 100vh; */
}

.logo {
    display: block;
    margin: 0 auto 2rem;
}

nav {
    width: 100%;
    font-size: 12px;
    text-align: center;
    margin-top: 2rem;
    z-index: 1;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
/* 
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
} */
</style>
