<template>
<transition appear name="slideout" type="transition">
  <section class="slideout">
    <div class="slideout__container">
     <h1 class="slideout__heading">Slideout</h1>
     <div class="slideout__player"></div>

     <div class="slideout__actions">
       <span>Sword</span>
       <span>shield</span>
       <span>arrow</span>
     </div>

    </div>
  </section>
</transition>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.slideout {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  background-color: #3d84a8;
  color: #ffffff;
  height: 100vh;
  width: 40%;
  max-width: 450px;
  display: flex;
  align-items: center;
  justify-content: center;

  &__container {
    height: 80%;
    width: 90%;
    text-align: center;
    background-color: #46cdcf;
    display: flex;
    flex-direction: column;
    align-items: center
  }

  &__player {
    margin-top: 2rem;
    height: 150px;
    width:150px;
    border-radius: 100%;
    background-color: #48466d;
  }

  &__actions {
    margin-top: 3rem;
    background-color: #48466d;
    width: 90%;
    display: flex;
    justify-content: space-around;
  }
}

.slideout-enter {
  transform: translateX(-500px)
}

.slideout-enter-active {
  transition: transform 0.8s;
}
</style>
