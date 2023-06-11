<template>
    <div>
        <Welcome />
        <h1>姓名：{{ name }}</h1>
        <h1>年龄：{{ age }}</h1>
        <h3>工作种类：{{ job.type }}</h3>
        <h3>工作薪水：{{ job.salary }}</h3>
        <button @click="set">点击更新页面</button>
    </div>
</template> 

<script>
import { ref } from 'vue'
import Welcome from './components/Welcome.vue'
export default {
    name: "App",
    setup() {
        //数据
        let name = ref("张三");
        let age = ref(18);
        let job = ref({
            type: '前端工程师',
            salary: '30k',
        })

        //方法
        function set() {
            name.value = "李四";
            age.value = 20;
            job.value.type = 'UI设计师'
            job.value.salary = '20k'
        }
        return {
            name,
            age,
            set,
            job
        };
    },
    components: { Welcome }
}
</script>

<style>

</style>
