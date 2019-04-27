<template>
    <div @dblclick="task.pending = !task.pending" :class="stateClass" class="task">
        <span @click.stop="$emit('taskDeleted', task)" class="close">x</span>
       <p> {{ task.name }} </p>

    </div>
</template>

<script>
export default {
    props: {
        task: {type: Object, required: true}
    }, 
    computed: {
        stateClass() {
            return {
                pending: this.task.pending,
                done: !this.task.pending
            }
        }
    }
}
</script>

<style>

.task {
    position: relative;
    box-sizing: border-box;
    width: 350px;
    height: 150px;
    padding: 10px;
    border-radius: 8px;
    font-size: 2rem;
    font-weight: 300;
    user-select: none; /*impede que o user selecione o conteúdo*/
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;

}

.pending {
    border-left: 12px solid #B73229;
    background-color: #F44339;
}

.done {
    color: #DDD;
    border-left: 12px solid #0A8F08;
    background-color: #4CAF50;
    text-decoration: line-through;
}

.pending .close {
    border-left: 12px solid #B73229;

}

.done .close {
    border-left: 12px solid  #0A8F08;

}

.close {
    position: absolute;
    right: 10px;
    top: 10px;
    font-size: 0.9rem;
    font-weight: 600;
    height: 10px;
    width: 10px;
    border-radius: 5px;
    display: flex;
    justify-content: center;
  
}

 
</style>
