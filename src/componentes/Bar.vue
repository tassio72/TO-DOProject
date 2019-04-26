<template>
    
    <div  class="barra-externa">
        {{ `${bar}%` }}  
        <div class='interna' :style="{'width': `${bar}%`}"> </div>
    </div>


</template>

<script>
// "
export default {

    data() {
		return {
			bar: '10'
		}
    },
    computed: {
        setBar() {

        }
    }

}
</script>

<style scoped>

    .barra-externa {
        width: 80%;
        height: 20px;
        border: 1px solid white;
        border-radius: 3px;
        position: relative;
        text-align: center;
        font-weight: 600;
    
    }

    .interna  {
        background: rgb(83, 212, 83);
        height: 100%;
        width: 70%;
        position: absolute;
        z-index: -1;
        left: 0;
        bottom: 0.0px;
    }
   
</style>
