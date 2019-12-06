<template>
    <div id="container">
        <p class="textColor-red font-bold">Hello. This is container contents test boundary!</p>
        <button class="bg-red-600 hover:bg-red-600 text-white font-bold py-2 px-4 rounded">
            Button
        </button>
        <p class="textColor-blue font-bold p-3 m-3">{{ msg }}</p>
        <p class="textColor-blue font-bold p-3 m-3">{{ weather }}</p>
    </div>

</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator'

@Component({
    props: {
        msg: String,
        weather: String,
    }
})
export default class Contents extends Vue {

}
</script>

<style scoped>

</style>