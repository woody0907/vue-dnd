<template>
    <div class="board" :id="id" @dragover.prevent @drop.prevent="drop">
        <slot/>
    </div>
</template>

<script>
export default {
    name:"Board",
    props:['id'],
    methods:{
        drop: e => {
            const card_id = e.dataTransfer.getData('card_id');
            console.log(card_id+"@@@@@@@@@@@");
            const card = document.getElementById(card_id);
            card.style.display="block";
            e.target.appendChild(card);
        }
    }
}
</script>

<style scoped>

</style>