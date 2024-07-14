<template>
  <main>
    <section id="presentation">
      <ThePresentation />
    </section>
    <section id="creations">
      <h2>Mes Projets</h2>
      <AllProjects/>
      <div>
      </div>
    </section>
    <section id="contact">
      <h2>Mon Contact</h2>
      <ContactForm />
    </section>
  </main>
</template>


<script setup>
  import ThePresentation from '../components/ThePresentation.vue'
  import AllProjects from '../components/AllProjects.vue'
  import ContactForm from '../components/ContactForm.vue'
</script>


<style scoped>
main{
  background-color:bisque;
  color:black;
}
#presentation {
  padding: 1rem;
  text-align: center;
}
h1 {
  font-size:50px;
}
h2 {
  font-size:40px;
}
#creations {
  padding: 1rem;
  text-align: center;
}
#contact {
  padding: 1rem;
  text-align: center;
}

</style>