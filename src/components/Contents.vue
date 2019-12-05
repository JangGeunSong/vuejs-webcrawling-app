<template>
    <div id="container">
        Hello. This is container contents test boundary!<br />
        {{ msg }}<br />
        <button class="bg-red-600 hover:bg-red-600 text-white font-bold py-2 px-4 rounded">
            Button
        </button>
    </div>

</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator'

@Component({
    props: {
        msg: String,
    }
})
export default class Contents extends Vue {

}
</script>

<style scoped>

</style>