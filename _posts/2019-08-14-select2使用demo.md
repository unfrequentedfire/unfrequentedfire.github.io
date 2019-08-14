---
layout: post
title: "select2使用demo"
date: 2019-08-14
tag: select2
---

### 1 导包

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190814153916.png)

### 2 页面

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/1565768393906.png)

### 3 js代码

```javascript
$("#ds_name").select2({
    placeholder:"请选择企业",
    language: "zh-CN",//设置语言，需要导包
    allowClear:true,//是否允许清空选择
   	data:[{
		id: "默认id", text: "默认值"
	}],//设置初始option
    ajax:{//获取远程数据
        dataType:'json',
        type:"post",
        url:MSysPath+"/company/page",
        data:function (params) {
            return{
                company_name:params.term,
                pageno:params.page || 1,
                orgid:xn_orgid
            };
        },
        processResults:function (result,params) {
            params.page = params.page || 1;
            var list=[];
            if(result && result.data){
                var data = result.data.pagelist;
                for(var i in data){
                    var obj = data[i];
                    list.push({
                        "id":obj.company_id,
                        "text":obj.company_name
                    })
                }
            }
            return{
                results:list,//[{id:"XX",text:"XX"},……]
                pagination: {
                    more: (params.page * 10) < result.data.totalcount
                }
            }
        }
    }
});
```

### 4 展示

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190814153600.png)



