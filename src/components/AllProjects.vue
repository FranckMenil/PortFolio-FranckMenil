<template>
    <div>
         <h2>Mes Projets</h2>
         <div class="projet1" @click="handleClick(projects[0])">
             <img src="/src/assets/pictures/image CV_Franck_Menil.png" alt="CV">
             <P>Création d'un CV en ligne </P>
         </div>
         <div class="projet2" @click="handleClick(projects[1])">
             <img src="/src/assets/pictures/picture_CahierDesCharges.png" alt="Cahier des charges">
             <P>Réalisation d'un cahier des charges </P>
         </div>
         <div class="projet3"@click="handleClick(projects[2])">
             <img src="/src/assets/pictures/picture_Commentaires.png" alt="Espace commentaires">
             <P>Dynamiser un espace de commentaires </P>
         </div>
         <TheModal :isOpen="isModalOpen" :project="selectedProject" @close="closeModal" />
     </div>
     
 </template>
 
 <script setup>
 import { ref } from 'vue'
 import TheModal from './TheModal.vue'
 
 const isModalOpen = ref(false)
 const selectedProject = ref(null)
 
 const projects = [
   { id: 1, 
     name: 'Projet 1', 
     description: `Création d'un CV en ligne` , 
     technologies:`Technologies utilisées : HTML5 et CSS3 ` ,
     picture:"/src/assets/pictures/CV_FranckMenil.png" ,
     cvLink: "https://github.com/FranckMenil/CV-FranckMenil"
 },
   { id: 2, 
     name: 'Projet 2', 
     description: `Réalisation d'un cahier des charges`, 
     technologies:`Technologies utilisées : WORD et FIGMA`,
     picture:"/src/assets/pictures/image_CahierDesCharges.png",
     documentLink: "/src/assets/documents/Cahier_des_charges_la_socketterie.pdf",
     
 },
 
   { id: 3, 
     name: 'Projet 3', 
     description: `Dynamiser un espace de commentaires`, 
     technologies:`Technologies utilisées : JavaScript`,
     picture:"/src/assets/pictures/image_Commentaires.png",
     ProjectJsLink:"https://github.com/FranckMenil/DynamiserUnEspaceDeCommentaires" 
 }]
 
 const handleClick = (project) => {
   selectedProject.value = project
   isModalOpen.value = true
 }
 
 const closeModal = () => {
   isModalOpen.value = false
 }
 
 </script>
 
 <style scoped>
 div {
    margin-top: 20em;
}
h2 {
  font-size: 40px;
}
 .projet1 {
     display: flex;
     justify-content:center;
     padding-right: 5em;
     margin: auto;
 }
 
 .projet2 {
     display: flex;
     justify-content:center;
     margin-top: 5em;
}
 
 .projet3 {
     display: flex;
     justify-content:center;
     margin-top: 5em;
     padding-left:2em;
 }
 
 img:hover {
     box-shadow: 10px 10px 20px rgba(214, 17, 17, 0.2);
 }
 
 img {
     height:20em;
     width: 32em;
     cursor: pointer;
 }
 
 p {
     padding-left:2%;
     font-size:20px;
 }
 </style>