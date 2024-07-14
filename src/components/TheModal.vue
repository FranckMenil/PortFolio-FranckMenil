<template>
    <div v-if="isOpen" class="modal" @click.self="close">
        <div class="modal-content">
            <button @click="close">X</button>
            <h2>{{ project.name }}</h2>
            <h3>{{ project.description }}</h3>
            <h3>{{ project.technologies }}</h3>
            <div v-if="project.cvLink">
                <a :href="project.cvLink" target="_blank">Lien GitHub</a>
            </div>
            <div v-if="project.documentLink">
                <a :href="project.documentLink" target="_blank">Téléchargement du Document</a>
            </div>
            <div v-if="project.ProjectJsLink">
                <a :href="project.ProjectJsLink" target="_blank">Lien GitHub</a>
            </div>
            <img :src="project.picture" alt="Project Image" />
            
        </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps, defineEmits } from 'vue'
  
  const props = defineProps({
    isOpen: {
      type: Boolean,
      required: true
    },
    project: {
      type: Object,
      default: null
    }
  })
  
  const emit = defineEmits(['close'])
  
  const close = () => {
    emit('close')
  }
  </script>
  
  <style scoped>
  .modal {
  position:fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}
  
.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  position: relative;
  
}
  
.modal-content-button {
  position:absolute;
  font-size: 1.5rem;
}


img {
  max-width: 70%;
  height: 100%;
  margin-top: 10px;
}
</style>
  