<template>
  <main>
    <section id="presentation">
      <ThePresentation />
    </section>
    <section id="creations">
      <AllProjects/>
      <div>
      </div>
    </section>
    <section id="contact">
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
#creations {
  padding: 1rem;
  text-align: center;
}
#contact {
  padding: 1rem;
  text-align: center;
}
</style>