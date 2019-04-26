<template>
    <div class="make-taks">
        
        <div class="btn">
            <input @keyup.enter="taks.push($event.target.value)" type="text" placeholder="Crie uma nova tarefa"/><button> + </button>
        </div>       

        <app-taks-new v-for='(tak, index) in taks' :key='index'> 
        <p> {{ tak }} </p>

        </app-taks-new >     


    </div>


</template>

<script>

import Taks from './Taks'

export default {
    components: {
        'app-taks-new': Taks
    },
    data() {
        return {
            taks: []
        }
    },
    methods: {
       
    },
    created() {
        console.log(this.taks)
    }
 
}
</script>

<style scoped>
    .make-taks {
        width: 15%;
        height: 25px;
        border: 1px solid white;
        border-radius: 3px;
        color: white;
        padding: 0%;
        margin-top: 10px;
    }

    .btn {
        width: 100%;
        height: 100%;
       
    }
    .btn input {
        width: 75%;
       
    }

    .btn button {
        width: 20%;
        
        height: 100%;
    }

</style>
