<script setup>
import { RouterLink } from 'vue-router'

defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <section>
    <header>
      <h1 class="title blink-title" :class="{'active': this.$route.name === 'home'}">
        <RouterLink to="/">Rafael Künstler</RouterLink>
        <span>presents</span>
      </h1>
    </header>
    <nav>
      <div class="item with-subitem">
        <RouterLink to="/about">Series</RouterLink>
        <div class="subitem blink-bigbang">
          <RouterLink to="/about">The Big Bang is made out of organized chaos ª•ª¶§∞∞∞››</RouterLink>
        </div>
      </div>
      <div class="item with-subitem">
        <RouterLink to="/about">Paintings</RouterLink>
        <div class="subitem blink-bigbang" :class="{'active': this.$route.name === 'auflassen'}">
          <RouterLink to="/canvas/auflassen">Auflassen (2022)</RouterLink>
        </div>
        <div class="subitem blink-bigbang">
          <RouterLink to="/about">Early works</RouterLink>
        </div>
      </div>
    </nav>
  </section>
</template>

<style scoped>
nav {
  margin-top: 80px;
  max-width: 80%;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

.title {
  margin: 0;
  margin-top: 11px;
  line-height: 26px;
}

.title a {
  /* color: red; */
  font-size: 28px;
  letter-spacing: -2px;
}

.title span {
  font-size: 20px;
  display: block;
  font-weight: 300;
}

.with-subitem {
  margin-bottom: 44px;
}

.item {
  
}

.item a {
  font-size: 14px;
}

.subitem {
  
}

.subitem a {
  font-size: 24px;
  letter-spacing: -1px;
}

.blink-bigbang {
  transition: all 0.2s ease;
}

.blink-bigbang:hover,
.blink-bigbang.active {
  transform: scale(1.2); 
  margin-left: 18px;
}

@media (max-width: 1320px) {
  .blink-bigbang:hover,
  .blink-bigbang.active {
    transform: scale(1); 
  }
}

.blink-bigbang a:hover,
.active.blink-bigbang a {
  background-color: hsla(0, 0%, 75%, 0.1);
  animation: color-change 0.8s step-end infinite;
}

.blink-title a:hover,
.active.blink-title a {
  background-color: hsla(0, 0%, 100%, 0.1);
  animation: color-change 0.4s step-start infinite;
}

@keyframes color-change {
  0% {
    color: #FE0A90;
  }
  20% {
    color: #67B3C4;
  }
  40% {
    color: #FE4400;
  }
  60% {
    color: #BB508A;
  }
  80% {
    color: #A9AAF9;
  }
  90% {
    color: #FE0A90;
  }
  100% {
    color: #DBFD3B;
  }
}
.blink-title {
  transition: all 0.2s ease;
}
.blink-title:hover,
.active.blink-title {
  transform: scale(1.2); 
  margin-left: 25px;
}

@media (max-width: 1320px) {
  .blink-title:hover,
  .active.blink-title:hover {
    transform: scale(1);
    margin-left: 0;
  }
}

/* .subitem a:hover {
  background-color: hsla(310, 100%, 37%, 0.2);
  color: black !important;
} */

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
