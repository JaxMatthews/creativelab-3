<template>
<div id="app">
  <div id="menu">
    <div id="brand">
      <router-link to="/">
        <img src="/images/projector.png">
      </router-link>
    </div>
    <div id="side">
      <router-link to="/browse">
        <div class="menu-item browse">
          <img src="/images/thumbsup.png">
          <p>Would Watch List</p>
        </div>
      </router-link>
      <router-link to="/yes">
        <div class="menu-item">
          <img src="/images/thumbsdown.png">
          <p>Would Not Watch</p>
        </div>
      </router-link>
    </div>
  </div>
  <router-view />
  <div class="footer-padding"></div>
    <div class="footer">
      <a href="https://github.com/JaxMatthews/creativelab-3">View GitHub Repository</a>
    </div>
</div>
</template>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 50px 100px;
  background: #8F4401;
}

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #B84901;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
  color: black;
}

#side img {
  width: 50px;
}

.menu-item {
  display: flex;
  flex-direction: column;
}

.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}

.footer-padding {
  height: 7vh;
}
.footer {
    display: flex;
    width: 100%;
    height: 7vh;
    justify-content: center;
    align-items: center;
    background-color: #8F4401;
    box-shadow: 0px -4px 5px rgba(0, 0, 0, 0.2);
    padding: 0.3em 0em;
    position: fixed;
    bottom: 0;
  }

  .footer a {
    margin: 0em 1em;
    color: #ffffff;
    font-size: 1em;
    text-decoration: none;
    border: 1px solid white;
    border-radius: 0.25em;
    padding: 0.2em;
  }
  .footer a:hover {
    border: 1px solid #000000;
    color: #000000;
  }
</style>
