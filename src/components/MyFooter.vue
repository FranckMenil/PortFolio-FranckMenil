<template>
    <footer>
    <div class="social-links">
        <a href="https://github.com/votreprofil" target="_blank" ><img src ="/src/assets/pictures/github.png" alt="github"></a>
        <a href="https://github.com/votreprofil" target="_blank"><img src ="/src/assets/pictures/linkedin.png" alt="linkedin"></a>
        <a href="https://github.com/votreprofil" target="_blank"><img src ="/src/assets/pictures/X.jpg" alt="X"></a>
    </div>
    <p>Dernière mise à jour : {{ lastUpdated }}</p>
  </footer>

</template>

<script>
    export default {
  data() {
    return {
      lastUpdated: new Date().toLocaleDateString()
    }
  }
}
</script>

<style scoped>
footer {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 1rem;
  background-color: #333;
  color: #fff;
  border-top: solid gray;
}
.social-links img {
    height: 50px;
    align-items: center;
}
.social-links a {
  color: #fff;
  margin-right: 1rem;
  text-decoration: none;
  transition: color 0.3s;
}

.social-links a:hover {
  color: #ddd;
}
</style>