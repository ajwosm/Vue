### axios

```
//安装axios
npm install axios    

//unpkg CDN
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>     

```



```vue
<script>
    //post请求
    axios.post('/地址',{
        .then(function(response)){
        	//请求成功的情况
	        console.log(response)
	    }
    }).catch(function (error){
        //请求失败的情况
        console.log(error)
    }).then(function(response){
        //请求失败或成功都会执行
        console.log(response)
	})
</script>
```



