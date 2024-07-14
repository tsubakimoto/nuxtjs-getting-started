<template>
    <div>
        <h1>現在の時刻</h1>
        <p>{{ currentTime }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            currentTime: new Date().toLocaleTimeString(),
        };
    },
    mounted() {
        setInterval(() => {
            this.currentTime = new Date().toLocaleTimeString();
        }, 1000);
    },
};
</script>

<style scoped>
h1 {
    color: #333;
}
</style>