<template>
  <div class="wrapper">
    <h1>good morning :]</h1>
    <img class="cat" src="https://c.tenor.com/4HleA7KDH-0AAAAC/tenor.gif" />
    <div class="align-left">
      <h1 class="align-left">im not bad at html anymore!!!</h1>
      <span> but you can still join my minecraft server!!!!!!!!! </span>
      <router-link to="/get-trolled" title="awesome minecraft!!"
        >https://discord.gg/spap</router-link
      >
    </div>
    <hr width="80%" />
    <span>looking for my other sites on spap.cloud?</span>
    <nav>
      <a href="https://tambourine.spap.cloud/">personal website</a>
      <a href="https://minesweeper.spap.cloud/">cat-themed minesweeper</a>
    </nav>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h1 {
  font-size: 57px;
}

.align-left {
  align-self: flex-start;
}

nav {
  display: block;
  width: 100%;
  text-align: center;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
}

img.cat {
  width: 100%;
  height: auto;
}
</style>
