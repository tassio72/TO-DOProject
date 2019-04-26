<template>
    
    <div class="barra-externa"> 
     {{ `${desempenho}%` }}  
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
        position: relative;
        text-align: center;
        font-weight: 600;
    
    }
    .barra-externa::after  {
        content: '';
        background: rgb(83, 212, 83);
        height: 100%;
        width: 70%;
        position: absolute;
        z-index: -1;
        left: 0;        
        
    }
   
   
</style>
