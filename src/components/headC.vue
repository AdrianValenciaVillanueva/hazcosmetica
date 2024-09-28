<template>
  <div class="frame">
    <header class="header">
      <div class="div">
        <p class="p">
          Producción de artículos de belleza personalizados bajo tu propia marca.
        </p>
        <button class="button-instance">Nuestro catálogo</button>
      </div>
      <div>
        <img class="imgH" src="../assets/logo.png" alt="" />
      </div>
    </header>

    <div class="hidden-text">
      <img class="imgH" src="../assets/logo.png" alt="" />
      <p class="p">
        Producción de artículos de belleza personalizados bajo tu propia marca.
      </p>
      <button class="button-instance">Nuestro catálogo</button>
    </div>
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
  display: flex;
  flex-direction: row;
  gap: 60px;
  position: relative;
  width: 100%;
  box-sizing: border-box;
  padding: 2vw 5vw;
}

.header {
  align-items: flex-start;
  background-color: transparent;
  display: flex;
  flex: 1;
  padding: 50px 0;
  position: relative;
  width: 100%;
  box-sizing: border-box;
}

.div {
  align-items: flex-start;
  display: flex;
  flex-direction: column;
  gap: 35px;
  position: relative;
  flex: 1;
}

.p {
  color: rgb(0, 0, 0);
  text-align: left; /* Alineación a la izquierda */
  font-family: 'Inter', sans-serif; /* Aplicando la fuente Inter */
  font-size: 30px;
  font-weight: 700; /* Manteniendo el texto en negritas */
  letter-spacing: 0;
  line-height: 28px;
  position: relative;
  max-width: 500px; /* Limitar el ancho del texto */
  margin: 0; /* Remover márgenes adicionales */
}

.button-instance {
  background-color: #A3A646;
  font-family: 'Inter', sans-serif;
  border: none;
  border-radius: 14px;
  width: 236px;
  height: 68px;
  position: relative;
  font-size: 20px;
  font-weight: 500; /* Ajusta el peso para el botón */
}

.imgH {
  height: auto;
  max-width: 100%;
  position: relative;
}

.hidden-text {
  display: none;
}

@media (max-width: 768px) {
  .frame {
    flex-direction: column;
    gap: 30px;
  }

  .header {
    padding: 20px 0;
  }

  .p {
    font-size: 18px;
    max-width: 100%;
  }

  .button-instance {
    width: 100%;
    height: auto;
    padding: 10px;
    font-size: 18px;
  }

  .imgH {
    width: 100%;
    height: auto;
  }
}

@media (max-width: 530px) {
  .header {
    display: none;
  }

  .hidden-text {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
  }

  .text-wrapper {
    font-size: 10vw;
  }
}
</style>
