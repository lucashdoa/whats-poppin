<template>
  <nav class="navigation">
    <ul>
      <li
        class="list"
        :class="{ active: activeTab === 'home' }"
        @click="activeTab = 'home'"
      >
        <a href="#">
          <span class="icon">
            <ion-icon name="home-outline"></ion-icon>
          </span>
          <span class="text">Home</span>
        </a>
      </li>
      <li
        class="list"
        :class="{ active: activeTab === 'liked' }"
        @click="activeTab = 'liked'"
      >
        <a href="#">
          <span class="icon">
            <ion-icon name="heart-outline"></ion-icon>
          </span>
          <span class="text">Liked</span>
        </a>
      </li>
      <li
        class="list"
        :class="{ active: activeTab === 'disliked' }"
        @click="activeTab = 'disliked'"
      >
        <a href="#">
          <span class="icon">
            <ion-icon name="heart-dislike-outline"></ion-icon>
          </span>
          <span class="text">Disliked</span>
        </a>
      </li>
      <div class="indicator"></div>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 'home',
    }
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900');

.navigation {
  width: 400px;
  height: 70px;
  background: #fff;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}
.navigation ul {
  display: flex;
}
.navigation ul li {
  position: relative;
  list-style: none;
  width: 60px;
  height: 60px;
  z-index: 1;
}
.navigation ul li a {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
  text-align: center;
  font-weight: 500;
}
.navigation ul li a .icon {
  position: relative;
  display: block;
  line-height: 75px;
  font-size: 1.5em;
  text-align: center;
  transition: 0.5s;
  color: var(--clr);
}
.navigation ul li.active a .icon {
  transform: translateY(-45px);
}
.navigation ul li a .text {
  position: absolute;
  color: var(--clr);
  font-weight: 400;
  font-size: 0.75em;
  letter-spacing: 0.05em;
  transition: 0.5s;
  opacity: 0;
  transform: translateY(20px);
}
.navigation ul li.active a .text {
  opacity: 1;
  transform: translateY(10px);
}
.indicator {
  position: absolute;
  top: -50%;
  width: 60px;
  height: 60px;
  background: #29fd53;
  border-radius: 50%;
  border: 6px solid var(--clr);
  transition: 0.5s;
}
.indicator::before {
  content: '';
  position: absolute;
  top: 50%;
  left: -22px;
  width: 20px;
  height: 20px;
  background-color: transparent;
  border-top-right-radius: 20px;
  box-shadow: 1px -10px 0 0 var(--clr);
}
.indicator::after {
  content: '';
  position: absolute;
  top: 50%;
  right: -22px;
  width: 20px;
  height: 20px;
  background-color: transparent;
  border-top-left-radius: 20px;
  box-shadow: 0 -10px 0 0 var(--clr);
}
.navigation ul li:nth-child(1).active ~ .indicator {
  transform: translateX(calc(60px * 0));
}
.navigation ul li:nth-child(2).active ~ .indicator {
  transform: translateX(calc(60px * 1));
}
.navigation ul li:nth-child(3).active ~ .indicator {
  transform: translateX(calc(60px * 2));
}
</style>
