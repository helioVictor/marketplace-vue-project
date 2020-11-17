<template>
  <header>

    <div id="header-top">
      <h1>{{ enterpriseName }}</h1>

      <div id="input-div">
        <select name="departmentSelect" id="department-select">
          <option value="Laptop" v-for="department in departments" :key="department.name">
            {{ department.name }}
          </option>
        </select>
        <input type="text">
      </div>

      <div class="right-side">
        <div class="login-field">
          <p>Olá, Faça seu Login.</p>
        </div>
        <div class="Cart" >
            <p>Carrinho</p>
        </div>
      </div>

    </div>

    <div id="header-bottom">
      <div class="address">
        <span>Diga qual seu endereço</span>
      </div>

      <div class="highlights" v-for="highlight in highlights" :key="highlight.name">
          <span>{{ highlight.name }}</span>
      </div>
    </div>

  </header>
</template>

<script>

export default {
  name: 'Header',
  props: {
    enterpriseName: String
  },
  data() {
    return {
      departments: [
        { name: 'Laptops' },
        { name: 'Hardware' }
      ],
      highlights: [
        { name: 'Bestselling' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  header {
    display: flex;
    flex-direction: column;

    width: 100%;
    height: 16vh;
    min-width: 100px;
    background-color: var(--dark-blue);
    color: var(--full-white);
    min-width: 600px;
    font-size: 1.5rem;
  }

  #header-top {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 60%;
  }



  #input-div {
    position: relative;
    width: 40%;
    min-width: 300px;
  }

  #input-div input {
    width: 100%;
    height: 4rem;
    border-radius: 0.6rem;
    padding-left: 16%;
    border: none;
  }

  #input-div select {
    position: absolute;
    height: 100%;
    border-radius: 0.6rem 0 0 0.6rem;
    border: none;
  }

  .right-side {
    display: flex;
    justify-content: space-evenly;
    width: 20vw;
  }

  #header-bottom {
    display: flex;
    align-items: center;
    height: 40%;
    background-color: var(--light-blue);
  }

  .address {
    width: 25%;
    padding: 1rem;
  }  

  .highlight {
    
  }


</style>
