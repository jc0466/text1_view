<template>
 <section class="section">
     <article class="hero"> 
         <div class="hero-body">
             <div class="container">
                 <h1 class="title">저는 {{dogName.toUpperCase()}}입니다.</h1>
                 <h2 class="subtitle">많이 사랑해주세요!</h2>
         </div>
     </article>
     {{dogname}}
 </section>
</template>
<script>
   export default {
     asyncData({params}) {
       return {
           dogname: params.dog
       }
     }
     };
</script>