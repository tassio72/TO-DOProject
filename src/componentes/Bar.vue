<template>
    
    <div class="barra-externa"> 
        <div class="barra-interna"> </div> 
        <p> {{ desempenho}}  </p>
    </div>


</template>

<script>
export default {

    data() {
		return {
			desempenho: '10'
		}
	}

}
</script>

<style>

    .barra-externa {
        width: 80%;
        height: 20px;
        border: 1px solid white;
        border-radius: 3px;

    }
    .barra-interna  {
        color: white;
        background: rgb(83, 212, 83);
        height: 100%;
        width: 70%;
        text-align: center;
        
        
    }

    .barra-interna p {
        margin: 0%;
        padding: 0%;
        position: absolute; 
        z-index: -1;
    }
   
   
</style>
