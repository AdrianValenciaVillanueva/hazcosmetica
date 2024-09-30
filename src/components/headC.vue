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
  width: 100%;
  box-sizing: border-box;
  padding: 0 6rem;
}

.main-text {
  display: flex;
  flex-direction: column;
  gap: 2em;
  width: 50%;
  height: auto;
}

.main-text p {
  color: rgb(0, 0, 0);
  text-align: left; /* Alineación a la izquierda */
  font-family: 'Inter', sans-serif; /* Aplicando la fuente Inter */
  font-size: 3.8vw;
  font-weight: 700; /* Manteniendo el texto en negritas */
  margin: 0; /* Remover márgenes adicionales */
  
}

.button-instance {
  background-color: #A3A646;
  font-family: 'Inter', sans-serif;
  border: none;
  border-radius: 14px;
  font-size: 1em;
  font-weight: 500;
  padding: 0.5em 1em;
  width: 50%;
}


.imgH {
  height: 40vw;
}


@media (max-width: 768px) {
  
  * {
    box-sizing: border-box;
  }
  .frame {
    flex-direction: column;
    padding:0;
  }
  .header {
    width: 100%;
    display: flex;
    justify-content: space-around; 
    align-items: start;
    padding: 0;
    margin-top: 2em;
    margin-left: .5em;
    margin-right: .5em;
  }
  .main-text {
    padding: 0;
    display: flex;
    flex-direction: column;
  }
  .main-text p {
    font-size: 2rem;
    padding-top: 0;
  }
  
  .imgH {
    height: 36vw;
  }
}

@media (max-width: 540px) {
 .header{
  background-color: blue;
 }
}
</style>
