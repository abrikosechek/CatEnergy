<template>
  <div class="intro">
    <div class="content container">
      <h1>Функциональное питание для котов</h1>
      <h4>ЗАНЯЛСЯ СОБОЙ? ЗАЙМИСЬ КОТОМ!</h4>
      <button><p>ПОДОБРАТЬ ПРОГРАММУ</p></button>
    </div>
    <img src="../assets/intro_food.png" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.intro {
  position: relative;
  display: flex;
  align-items: center;

  background-image: url("../assets/intro_bg.png");
  background-position: right center;
  background-size: auto 100%;
  background-repeat: no-repeat;
  min-height: 700px;

  img {
    position: absolute;
    left: 45%;
    top: 50%;
    transform: translateY(-50%);
  }

  .content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    gap: 30px;

    h1 {
      max-width: 450px;
    }
    h4 {
      max-width: 450px;
    }
    button {
      padding: 14px 20px;
      border: none;
      background-color: #68b738;
      & > p {
        font-size: 18px;
        color: white;
      }
    }
  }
}
</style>
