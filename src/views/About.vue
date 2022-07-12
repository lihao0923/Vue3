<template>
    <div id="About">
        <h1>About</h1>
        <button class="btn">count: {{count}}</button>

    </div>
</template>
<script>
import { ref } from 'vue';
export default {
    name: 'About',
    // 入口
    setup () {
        let count = ref(0);

        setInterval(() => {
            count.value++;
        }, 1000);

        return { count };
    }
}
</script>

<style>
#About {
    background-color: #fff;
}

.btn {
    padding: 5px 25px;
    cursor: pointer;
    font-size: 200px;
    border-radius: 10px;
}
</style>
