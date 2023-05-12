<template>
    <div id="app">
        <!--        <HelloWorld msg="Welcome to Your Vue.js App"/>-->
        <ChooseAndCreateTags :default-options="defaultOptions" :option-description="optionDescription"/>
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ChooseAndCreateTags from "@/components/ChooseAndCreateTags.vue";

export default {
    name: 'App',
    components: {
        HelloWorld,
        ChooseAndCreateTags
    },

    data() {
        return {
            defaultOptions: [
                {value: "option1", label:"option1"},
                {value: "option2", label:"option2"},
                {value: "option3", label:"option3"},
            ],
            optionDescription: "add an option"
        }
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
