<template>
    <div>
        <ul>
            <li v-for="n in number" :key="n" @click="change(n)">{{n}}</li>
        </ul>
      
    </div>
</template>

<script>
    export default {
        data ()  {
            return {
              number: [97, 98, 99, 100]
            }
        },
        methods: {
            change(n) {
                this.$emit("input", n)
            }
        }
    }
</script>

<style>
</style>


