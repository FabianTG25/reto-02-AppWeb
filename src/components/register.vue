<script setup>
import { ref } from 'vue';

const username = ref('');
const email = ref('');
const password = ref('');
const passwordConf = ref('');
const userType = ref('user');

const register = () => {
  // Aquí puedes implementar la lógica de registro
  console.log(`Username: ${username.value}, Password: ${password.value}, User Type: ${userType.value}`);
};
</script>

<template>
  <form @submit.prevent="register">
    <label>
      Nombre:
      <input type="text" v-model="username" required>
    </label>
    <label>
      Correo Electrónico:
      <input type="text" v-model="email" required>
    </label>
    <label>
      Contraseña:
      <input type="password" v-model="password" required>
    </label>
    <label>
      Confirmar Contraseña:
       <input type="password" required>
    </label>
    <label>
      Tipo de usuario:
      <select v-model="userType">
        <option value="user">Usuario</option>
        <option value="admin">Administrador</option>
      </select>
    </label>
    <button type="submit">Registrarse</button>
    <button type="button">
      <router-link to="/login">Iniciar sesión</router-link>
    </button>
  </form>
</template>

<style scoped>

form {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f7f7f7;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 10px;
  font-size: 14px;
  color: #333;
}

input[type="text"],
input[type="password"],
select {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 14px;
}

input[type="text"]:focus,
input[type="password"]:focus,
select:focus {
  border-color: #007BFF;
  box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
  outline: none;
}

button[type="submit"] {
  width: 100%;
  padding: 10px;
  background-color: #007BFF;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}

button[type="submit"]:hover {
  background-color: #0056b3;
}

button[type="button"] {
  width: 100%;
  padding: 10px;
  background-color: #6c757d;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}

button[type="button"]:hover {
  background-color: #5a6268;
}

button[type="button"] a {
  color: inherit;
  text-decoration: none;
  display: block;
}

button[type="button"] a:hover {
  text-decoration: none;
}

</style>