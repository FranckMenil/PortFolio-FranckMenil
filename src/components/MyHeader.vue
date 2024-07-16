<template>
    <header>
        <div class="photo">
            <a href="#" style = "padding:0;">
                <img src="/src/assets/pictures/FranckM.jpg" alt="Photo">
            </a>
        </div>  
        <nav>
            <ul>
                <li><a href="#presentation">Présentation</a></li>
                <li><a href="#creations">Projets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

</template>

<script>

</script>

<style scoped>
header {
  top: 0;
  position:fixed;
  width:100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 1rem;
  background-color: #333;
  color: #fff; 
}

.photo img{
    height: 250px;
    border-radius: 50%;
    box-shadow: 0 0 10px#dbc2a4;
    cursor: pointer;
    
}

ul , li , a {
    display: flex;
    color: white;
    list-style: none;
    text-decoration: none;
    padding: 3em 3em 0em 0em;
    font-size: 20px;
}

nav ul li a:hover {
  text-decoration: underline;
}

</style>