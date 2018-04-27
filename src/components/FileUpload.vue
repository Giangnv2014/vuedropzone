<template>
 <div id="app2">
   <vue-dropzone id="drop1" :options="config" @vdropzone-complete="afterComplete"></vue-dropzone>
 </div>
</template>

<script>
import vueDropzone from "vue2-dropzone";

export default {
 data: () => ({
   config: {
     url: "http://localhost:8000/api/image",
   }
 }),
 components: {
   vueDropzone
 },
 methods: {
   afterComplete(file) {
     console.log(file);
   }
 }
};
</script>
