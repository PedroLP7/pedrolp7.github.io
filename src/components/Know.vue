<template >
    <div>
       
            <P :class="{'textLight': lights, 'textDark': !lights}"> PRUEBA</P>


            <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='spanish'"> Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
        Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took 
        a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also
         the leap into elect.</p>

         <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='english'"> this is in english</p>
            <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='catalan'"> aixo es en catala</p>
            
       
   

    
        
    </div>
</template>
<script>
export default {
    name: 'Aboutme',
    props: {
       language: String,
       lights: Boolean
    },
    
}
</script>
<style scoped>
    p{
        font-size: 20px;
        
        margin: 20px;
        width: 50%;
        
    }
    
    .container{
        position: absolute;
        top: 30%;
        left: 40%;
        width: 50%;
    }

    
</style>