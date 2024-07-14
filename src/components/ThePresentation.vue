<template>
    <div>
        <h1>{{name}}</h1>
        <h2>Ma Présentation</h2>
        <h2>Bonjour !</h2>
        <p>Passionné, je me suis spécialisé en HTML , CSS et en JavaScript, en particulier avec le Framework VueJS.</p>
        <p>J'ai travaillé sur divers projets, allant de sites web pour petites entreprises à des plateformes spécifiques pour de grandes entreprises.</p>
        <p>Je porte une attention toute particulière à la création de sites internet responsive compatible mobile (Android, Iphone, Tablette...), <br>facile à prendre en main, avec une base de conception maintenable et à jour.</p>
    </div>

</template>

<script>
export default {
   data(){
    return {
        name: 'Franck MENIL',
    } 
   }
}
</script>

<style scoped>
h1 {
    font-size: 60px;
}
h2 {
    font-size: 40px;
}
p {
    text-align: start;
    margin-left:auto;
    margin-right:auto;
    width: 50em;
    font-size:larger;
}
</style>