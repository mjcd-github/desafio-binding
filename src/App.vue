<script>
export default {
  name: "App",
  data() {
    return {
      titulo:"",
      chip:"",
      numero:"",
      fecha:"",
      propietario:"",
      tipo:""

    };
  },
};
</script>

<template>
  <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input type="text" v-model="titulo" >
        </div>

        <div>
          <label>Chip SRC: </label>
          <input type="text" v-model="chip">
        </div>

        <div>
          <label>Número: </label>
          <input type="text" v-model="numero">
        </div>

        <div>
          <label>Fecha de expiración: </label>
          <input type="text" v-model="fecha">
        </div>

        <div>
          <label>Propietario: </label>
          <input type="text" v-model="propietario">
        </div>

        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input type="text" v-model="tipo">
        </div>
      </form>

      <div class="carnet">
        <h3>{{titulo}}</h3>
        <img width="40" :src="chip" alt="" />
        <div>
          <h2>{{ numero }}</h2>
          <span>Fecha Exp: <b>{{ fecha }}</b></span>
        </div>
        <footer>
          <span>{{ propietario }}</span>
          <img :src="tipo" width="60" />
        </footer>
      </div>
    
</template>

<style>
* {
        margin: 0;
      }
      body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 60vh;
        font-size: 10px;
        font-family: sans-serif;
      }

      #app {
        display: flex;
        gap: 40px;
      }
      form {
        padding: 18px;
        border-radius: 20px;
        border: ridge 1px;
        box-shadow: 1px 1px 1px 1px gray;
        font-weight: bold;
        display: flex;
        flex-direction: column;
        gap: 15px;
        justify-content: center;
      }
      form div {
        display: grid;
        grid-template-columns: 100px 200px;
        align-items: center;
        gap: 5px;
      }

      form div label {
        text-align: right;
      }

      .carnet {
        width: 400px;
        height: 230px;
        background: #1c1a1e;
        color: white;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 0px 0px 10px 2px black;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      h3 {
        font-size: 20px;
      }

      h2 {
        font-size: 30px;
        letter-spacing: 10px;
        margin-bottom: 15px;
        text-shadow: 0px 0px 1px gold;
        font-family: Times;
      }

      b {
        font-size: 16px;
      }

      footer {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        font-weight: bold;
        font-size: 18px;
        text-transform: uppercase;
        font-style: italic;
      }
</style>
