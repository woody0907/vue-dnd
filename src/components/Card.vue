<template>
    <div :id="id" :draggable="draggable" class="card" @dragstart="dragStart" @dragover.stop>
        <slot/>
     </div>
</template>

<script>
export default {
    name:"Card",
    props:['id','draggable'],
    methods:{
        dragStart:e=>{
            const target = e.target;
            e.dataTransfer.setData("card_id",target.id);
            setTimeout(()=>{
                target.style.display='none'
            },0)
        }
    }
}
</script>