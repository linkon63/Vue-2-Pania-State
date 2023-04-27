<template lang="">
    <div class="task">
        <h1>{{task.title}}</h1>
        <div class="icons">
            <i class="material-symbols-outlined" @click="taskStore.deleteTask(task.id)">
            delete_forever
            </i>
            <i class="material-symbols-outlined" @click="taskStore.toggleFav(task.id)"
            :class="{activeFav : task.isFav}"
            >
            favorite
            </i>
        </div>
    </div>
</template>
<script>
import { useTaskStore } from '../stores/TaskStore';

export default {
    props: ['task'],
    setup(props) {
        const taskStore = useTaskStore()

        return { taskStore }
    }
}
</script>
<style lang="">
    
</style>