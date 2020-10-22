<template>
    <div>
        {{name}} - {{description}} - {{isActive}}
    </div>
</template>

<script>
export default {
    name: "User",
    props: ['name', 'description', 'isActive']
}
</script>

<style scoped>

</style>