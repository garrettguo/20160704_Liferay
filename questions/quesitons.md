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