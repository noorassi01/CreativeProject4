<template>
<div id="app">
  <div class="header">
    <router-link to="/">
      <div class="logo">
        <img src="/ordinary.png" style="height: 100%; width: 300px">
      </div>
    </router-link>
  </div>
  <div class="content">
    <router-view />
  </div>
  <div class="footer">
    <p class="copyWrite">
      Noor Assi&copy; 2020
    </p>
    <ul class="footer-nav">
      <li><router-link to="/admin">Admin</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><a href="https://github.com/noorassi01/creative4"> Github rep</a></li>
    </ul>
  </div>
</div>
</template>

<style>
html {
  box-sizing: border-box;
}

body {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  background: #fff;
  padding: 0px;
  margin: 0px;
}

/* Header */
.header {
  display: flex;
  padding: 10px 100px 0px 100px;
  background-color: #F5B7B1;
  color: #1C454F;
  align-items: center;
  justify-content: center;
  text-decoration: none;
}

#app{
background-color: #F5B7B1;
}

.title {
  margin-top: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.title link{
  text-decoration: none;
}

.title h1 {
  font-size: 50px;
}

.content {
  padding: 20px 100px;
  min-height: 500px;
}

.footer-nav li + li{
  margin-left: 10px;
}

/* Footer */
.footer {
  height: 70px;
  padding: 20px 100px 0px 100px;
  background: #e3e3e3;
  font-size: 12px;
}
.copyWrite{
  float: left;
  font-size: 20px;
}
.footer-nav{
  list-style: none;
  float: right;
}
.footer-nav li{
  float: left;
  font-size: 20px;
}



.footer a {
  color: #000;
}

h1 {
  font-size: 20px;
}

h2 {
  font-size: 14px;
}
</style>
