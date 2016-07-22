* When I bind the onclick with JS twice, how to deal with the reflect?  
Firstly, unbinding the event and then bind the another event.
```
$(".content.$randomNamespace").unbind("click").on("click", "li .faq-question", function(){
        var answer = $(this).next(".answer");
        answer.slideToggle();
    });
```  
***
* Steps of submiting the code?
```
1.create the orgin branch `feat1`
2.use `git pull --all`
3.‘git checkout feat1’
4.put the modified things into local branch `feat1`
5.`git add -A`
6.`git commit -m "..."`
7.`git push origin feat1`
8.if just has one commit, you can use `git fetch --all`
9.use `git rebase origin/develop`
10.use `git push origin feat1`
```
***
* How to change the commit message?  
```
git commit --amend -m "Story HSF3-216 #comment Create FAQ pages."
```
***
* 如何生成git密钥？  
```
ssh-keygen
```
***
* el表达式中的`[]`是什么意思？  
```
${user.name} <==> ${user[name]}
```
若属性名中出现了特殊字符，如"."或者"-"等，这时就必须使用`[]`以避免语法上的冲突
***
* 如何查看某一个进程是否还在运行？
例如：
```
ps -aux | grep tomcat
```
***
* Liferay中的"Custome fields"有什么用法？  

用来控制role。
***
* Liferay中Custom-sql的用法？
`https://dev.liferay.com/develop/tutorials/-/knowledge_base/6-2/developing-custom-sql-queries`  
`http://www.programcreek.com/java-api-examples/index.php?api=com.liferay.util.dao.orm.CustomSQLUtil`  
***
* jstl中的functions  
`http://www.360doc.com/content/12/1112/10/11018021_247347185.shtml`
***
* liferay中`<liferay:ui message key="xxx">`的用法  
step1: 首先在`portlet.xml`中的`<supports>`标签中加入如下定义：  
```
<resource-bundle>content.Language</resource-bundle>
```
step2:  在`Language.properties`文件中加入key,value，其中key就是`<liferay:ui message key="xxx">`中的key，value就是你要替换的值。
***
* 怎样在linux中强制停止某一个进程？  
```
sudo pkill -9 java
```
***
* Java中如何对Map排序？
```
Map<String, String> map = new TreeMap<>(new Comparetor<String>(){
    @override
    ...
    ...
});
```
***
* linux中postgres的配置文件的位置？  
```
/var/lib/pgsql/9.4/data/pg_hba.conf
```
