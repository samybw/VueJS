<template>
    <div class="item-todo">
        <p>{{ tache }}</p>
        <button class="btn-supr" v-on:click="suppression">X</button>
    </div>
</template>

<script>
export default {
    name: 'Item',
    props: ['tache','suppression']
}
</script>

<style scoped>

    .item-todo {
        position: relative;
        padding : 20px 60px 20px 30px;
        font-size: 20px;
        height: 88px;
    }

    .btn-supr {
        position: absolute;
        top: 10px;
        right: 10px;
    }

    
</style>