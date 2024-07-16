<template>
    <h2>Mon Contact</h2>
    <form @submit.prevent="sendEmail">
        <div>
            <label for="name">Nom/Prénom</label>
            <input type="text" id="name" v-model="form.name" required>
        </div>
        <div>
            <label for="subject">Objet</label>
            <input type="text" id="subject" v-model="form.subject" required>
        </div>
        <div>
            <label for="message">Message</label>
            <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit">Envoyer</button>
  </form>

</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
  sendEmail() {
    let dotEnv = "franckmenil@gmail.com";
    console.log("Email destination:", dotEnv);


    alert('Email envoyé à ' + dotEnv);
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  max-width: 600px;
  margin: 0 auto;
  padding: 1rem;
}

div {
  margin-bottom: 1rem;
}

label {
  margin-bottom: 0.5rem;
  font-weight: bold;
}
h2 {
  font-size:40px;
}

input,
textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
    width: 100px;
    margin: auto;
  padding: 0.5rem 0.5rem;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #555;
}
</style>