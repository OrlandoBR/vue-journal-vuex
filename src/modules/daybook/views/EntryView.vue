<template>
  <div class="entry-title d-flex justify-content-between p-2">
      <div>
        <span class="text-success fs-3 fw-bold">15</span>
        <span class="mx-1 fs-3">Julio</span>
        <span class="mx-2 fs-4 fw-light">2022</span>
      </div>
      <div>
        <button class="btn btn-danger mx-2">
              Borrar
              <i class="fa fa-trash-alt"></i>
        </button>
                <button class="btn btn-primary">
              Subir Fotografia
              <i class="fa fa-upload"></i>
        </button>
       
      </div>
  </div>
  <hr>
  <div class="d-flex flex-column px-3 h-75">
      <textarea placeholder="¿Que sucedio hoy?"></textarea>
  </div>
 <FaB icon="fa-save" />
 <img src="https://photopxl.com/pxl-content/uploads/2019/06/3.-Vermilion-Lakes-Banff-NP.jpg" alt="entry-picture" class="img-thumbnail">
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {
components:{
    FaB: defineAsyncComponent(()=>import('../components/FaB.vue'))
}
}
</script>

<style lang="scss" scoped>
textarea{
font-size: 20px;
border:none;
height: 100%;

&:focus{
    outline: none;
}
}

img{
    width: 200px;
    position: fixed;
    bottom: 150px;
    right:20px;
}
</style>