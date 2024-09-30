<template>
  <div class="frame">

    <header class="header">

      <div class="main-text">
        <p>
          Producción de artículos de belleza personalizados bajo tu propia marca.
        </p>
        <button class="button-instance">Nuestro catálogo</button>
      </div>

      <div class="carousel">
        <img class="imgH" src="../assets/image 4.png" alt="" />
      </div>

    </header>

  </div>
</template>

<script>
export default {
  name: "HeadFrame",
  components: {},
};
</script>

<style scoped>
/* Importa la fuente directamente */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap');

.frame {
  align-items: center;
  justify-content: space-around;
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  width: 100%;
  padding: 2vw 5vw;
}

.header {
  align-items: center;
  display: flex;
  position: relative;
  width: 100%;
  box-sizing: border-box;
  margin-top: 0rem;
  padding-left: 6rem;
}

.main-text {
  display: flex;
  flex-direction: column;
  gap: 60px;
  width: 50%;
  height: auto;
}

.main-text p {
  color: rgb(0, 0, 0);
  text-align: left; /* Alineación a la izquierda */
  font-family: 'Inter', sans-serif; /* Aplicando la fuente Inter */
  font-size: 3rem;
  font-weight: 700; /* Manteniendo el texto en negritas */
  margin: 0; /* Remover márgenes adicionales */
  padding-top: 3.5rem;
}

.button-instance {
  background-color: #A3A646;
  font-family: 'Inter', sans-serif;
  border: none;
  border-radius: 14px;
  width: 236px;
  height: 68px;
  font-size: 20px;
  font-weight: 500; /* Ajusta el peso para el botón */
}


.imgH {
  height: 25rem;
}




</style>
