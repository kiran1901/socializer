<script setup>
defineProps({

})
</script>

<template>
    <div class="header">
        <a href="" class="logo">Socializerr</a>
        <input class="menu-btn" type="checkbox" id="menu-btn" />
        <label class="menu-icon" for="menu-btn"><span class="navicon"></span></label>
        <ul class="menu">
            <li><a href="#work">Chumma</a></li>
            <li><a href="#about">Try Pro</a></li>
            <li><a href="#careers">Notifications</a></li>
            <li><a href="#contact">Profile</a></li>
        </ul>
    </div>
</template>

<style scoped>
a {
  color: #2BAE66;
}

/* header */
.header {
    background-color: #FCF6F5;
    box-shadow: 1px 1px 4px 0 rgba(0,0,0,.1);
    position: fixed;
    width: 100%;
    z-index: 3;
}

.header ul {
  margin: 0;
  padding: 0;
  list-style: none;
  overflow: hidden;
  background-color: #FCF6F5;
  color: #2BAE66;
}

.header li a {
  display: block;
  padding: 20px 20px;
  border-right: 1px solid #f4f4f4;
  text-decoration: none;
  color: #2BAE66;
  transition: color 0.3s ease; /* Add transition for text color */
}

.header li a:hover,
.header .menu-btn:hover {
  background-color: #f4f4f4;
}

.header .logo {
    display: block;
    float: left;
    font-size: 2em;
    padding: 10px 20px;
    text-decoration: none;
    transition: color 0.3s ease; /* Add transition for text color */
}

/* menu */
.header .menu {
  clear: both;
  max-height: 0;
  transition: max-height 0.3s ease-out; /* Add transition for max-height */
}

/* menu items */
.header li {
  transition: transform 0.3s ease-out; /* Add transition for menu items */
}

.header .menu-btn:checked ~ .menu {
  max-height: 240px;
  transition: max-height 0.3s ease-in; /* Add transition when menu opens */
}

.header .menu-btn:checked ~ .menu li {
  transform: translateY(0); /* Shift menu items vertically when menu opens */
}

/* menu icon */
.header .menu-icon {
  cursor: pointer;
  display: inline-block;
  float: right;
  padding: 28px 20px;
  position: relative;
  user-select: none;
  transition: transform 0.3s ease; /* Add transition for menu icon */
}

.header .menu-icon .navicon {
  background: #333;
  display: block;
  height: 2px;
  position: relative;
  transition: background 0.3s ease; /* Add transition for background color */
  width: 18px;
}

.header .menu-icon .navicon:before,
.header .menu-icon .navicon:after {
  background: #333;
  content: '';
  display: block;
  height: 100%;
  position: absolute;
  transition: all 0.3s ease; /* Add transition for all properties */
  width: 100%;
}

.header .menu-icon .navicon:before {
  top: 5px;
}

.header .menu-icon .navicon:after {
  top: -5px;
}

/* menu btn */
.header .menu-btn {
  display: none;
}

.header .menu-btn:checked ~ .menu {
  max-height: 240px;
  transition: max-height 0.3s ease-in;
}

.header .menu-btn:checked ~ .menu-icon .navicon {
  background: transparent;
}

.header .menu-btn:checked ~ .menu-icon .navicon:before {
  transform: rotate(-45deg);
}

.header .menu-btn:checked ~ .menu-icon .navicon:after {
  transform: rotate(45deg);
}

.header .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:before,
.header .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:after {
  top: 0;
}

/* 48em = 768px */
@media (min-width: 48em) {
  .header li {
    float: left;
  }
  .header li a {
    padding: 20px 30px;
  }
  .header .menu {
    clear: none;
    float: right;
    max-height: none;
  }
  .header .menu-icon {
    display: none;
  }
}

</style>
