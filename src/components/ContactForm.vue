<template>
  <div class="contact-form">
    <h2>Contactez-nous</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Nom</label>
        <input type="text" id="name" v-model="formData.name" required />
      </div>
      <div class="form-group">
        <label for="firstname">Prénom</label>
        <input
          type="text"
          id="firstname"
          v-model="formData.firstname"
          required
        />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="formData.email" required />
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" v-model="formData.message" required></textarea>
      </div>

      <!-- Bouton pour afficher le récapitulatif -->
      <button type="submit">Envoyer et Afficher le récapitulatif</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: "",
        email: "",
        message: "",
      },
      recap: "", // Variable pour stocker le récapitulatif du formulaire
    };
  },
  methods: {
    submitForm() {
      // Envoyez les données du formulaire à votre serveur ou effectuez d'autres actions nécessaires ici.
      console.log("Formulaire soumis avec les données : ", this.formData);

      // Créez un récapitulatif du formulaire
      this.recap =
        "Récapitulatif du formulaire :\n\n" +
        `Nom: ${this.formData.name}\n` +
        `Prénom: ${this.formData.firstname}\n` +
        `Email: ${this.formData.email}\n` +
        `Message: ${this.formData.message}\n`;

      // Ouvrez une nouvelle fenêtre pour afficher le récapitulatif
      const recapWindow = window.open("", "_blank");
      recapWindow.document.write("<pre>" + this.recap + "</pre");
      recapWindow.document.close();

      // Réinitialisez le formulaire
      this.formData = {
        name: "",
        email: "",
        message: "",
      };
    },
  },
};
</script>

<style scoped>
.contact-form {
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  max-width: 900px;
  margin: 0 auto;
}

.form-group {
  margin-bottom: 15px;
  margin-top: 50px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 30px;
}

input,
textarea {
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 5px;
  width: 880px;
}

button {
  background-color: #cccccc;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

/* Style pour les erreurs de validation */
.error-message {
  color: #ff0000;
  font-size: 14px;
  margin-top: 5px;
}
</style>
