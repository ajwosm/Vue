<!--author:steam-404-->
<template>
<button @click="githubapi()">api.github.com请求</button>
<!--  创建请求按钮-->
</template>
<script>
import axios from 'axios'
// 导入axios
export default{

    // 方法
    methods:{

        // 方法
        githubapi(){
            axios({
                // 请求方式
                method:'get',
                // 请求url
                url:'https://api.github.com/'
            })
            .then(response=>{
                // 返回成功在控制台打印信息
                console.log(response);
            })
        }
    }
}
</script>