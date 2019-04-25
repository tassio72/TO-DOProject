<template>
    
    <div class="barra-externa">
        <div class="barra-interna">
         <p> {{ desempenho}} </p> 
        </div>
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
        display: flex;
        justify-content: center;
        width: 80%;
        height: 20px;
        border: 1px solid white;
        border-radius: 3px;

    }
    .barra-externa .barra-interna  {
        color: white;
        display: flex;
        justify-content: center;
        text-align: center;
        align-items: center
    }

</style>
