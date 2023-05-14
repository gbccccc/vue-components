<template>
    <div id="app">
        <!--        <HelloWorld msg="Welcome to Your Vue.js App"/>-->
<!--        <MultipleCreateAndSelect v-model="options" :default-options="defaultOptions" :option-description="optionDescription"-->
<!--                                 create-description="other option"/>-->
        <SelectAndCreateTags v-model="options" :default-options="defaultOptions" :option-description="optionDescription"/>
        {{ options }}
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SelectAndCreateTags from "@/components/SelectAndCreateTags.vue";
import MultipleCreateAndSelect from "@/components/MultipleCreateAndSelect.vue";

export default {
    name: 'App',
    components: {
        SelectAndCreateTags,
        HelloWorld,
        MultipleCreateAndSelect
    },

    data() {
        return {
            defaultOptions: [
                {value: "option1", label: "option1"},
                {value: "option2", label: "option2"},
                {value: "option3", label: "option3"},
            ],
            optionDescription: "add an option",
            options: []
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
