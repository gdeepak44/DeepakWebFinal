<template>
    <div class="header">
        <h1>
            {{ heading }}
        </h1>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        heading: String
    }
};
</script>

<style scoped>

.header{
    place-items: center;
}
</style>
