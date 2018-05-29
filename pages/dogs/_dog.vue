<template>
 <section class="section">
     <article class="hero"> 
         <div class="hero-body">
             <div class="container">
                 <h1 class="title">저는 {{dogName.toUpperCase()}}입니다.</h1>
                 <h2 class="subtitle">많이 사랑해주세요!</h2>
         </div>
         </div>
     </article>
     <article class="notification">
       <figure class="image is-square">
          <img :src="image" alt="">
       </figure>
     </article>
 </section>
</template>
<script>
  import axios from 'axios';
  
   export default {
     asyncData({params}) {
         const image = await axios.get();

       return {
           dogname: params.dog,
           image: image.data.message
       };
     }
     };
</script>