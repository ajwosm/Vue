<template>
    <div>
        <Welcome/>
        <h1>姓名：{{ person.name }}</h1>
        <h1>年龄：{{ person.age }}</h1>
        <h3>工作种类：{{ person.job.type }}</h3>
        <h3>工作薪水：{{ person.job.salary }}</h3>
        <h3>a:{{ person.job.a.b.c }}</h3>
        <h3>爱好：{{ person.hobby }}</h3>
        <button @click="set">点击更新页面</button>
    </div>
</template>

<script>
import { reactive } from 'vue'
import Welcome from './components/Welcome.vue'

export default {
    name: "App",
    setup() {
        //数据
        // let name = ref("张三");
        // let age = ref(18);
        // let job = reactive({
        //     type: '前端工程师',
        //     salary: '30k',
        //     a: {
        //         b: {
        //             c: 5,
        //         }
        //     }
        // })
        // let hobby = reactive(['抽烟','喝酒','烫头'])
        let person = reactive({
            name: "张三",
            age: 18,
            job: {
                type: '前端工程师',
                salary: '30k',
                a: {
                    b: {
                        c: 5,
                    }
                }
            },
            hobby: ['抽烟', '喝酒', '烫头']
        })

        //方法
        function set() {
            person.name = "李四";
            person.age = 20;
            person.job.type = 'UI设计师'
            person.job.salary = '20k'
            person.job.a.b.c = '10'
            person.hobby[0] = '学习'
        }

        return {
            person,
            set

        };
    },
    components: {Welcome}
}
</script>

<style>

</style>
