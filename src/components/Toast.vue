<template>
  <div class="toast"  :class="toast.type">
      <p>{{toast.text}}</p>
  </div>
</template>

<script>
export default {
    props:{
        toast:{type:Object}
    }
}
</script>

<style scoped>
    .toast{
        margin: 2rem;
        padding: 0.8rem;
        min-width: 30vh;
        text-align: center;
        background-color: rebeccapurple;
        color: #fff;
        border-radius: 5px;
    }
    .success{
        background-color: rgb(147, 231, 147);
        color: rgb(70, 68, 71);
    }
    .danger{
        background-color: rgb(236, 82, 43);
    }
    .warning{
        background-color: rgb(250, 226, 87);
    }
</style>>

