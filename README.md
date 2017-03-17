# git工具用法

## git 提交
```

（打包）git add .  //提交全部    git add 文件名// 提交指定文件
 
（描述）git commit -m "描述内容"
 
（发送）git push


```

* 上传 并且加载新项目：

```
git remote -v 查看远程仓库    

git pull upstream   拉回上游分支    

git checkout dev  切换到分支到dev   

git merge upstream/dev   (合并项目)  

git pull upstream 拉回上游分支   

git init       加载package.json 文件   

npm run dev    运行分支


```

# github 
1. 密钥生成

ssh-keygen -t rsa -C "1592096012@qq.com"  //-c "邮箱名"

2. 密钥添加
/Users/mac/.ssh/id_rsa_github  //输入保存密钥的地址；意思是在mac下的github 文件下

```
~/.ssh   //进入密钥


 ~ ssh-keygen -t rsa -C "1592096012@qq.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/mac/.ssh/id_rsa): /Users/mac/.ssh/id_rsa_guthub
Enter passphrase (empty for no passphrase):


 // 1 Host showgold.cn
Enter same passphrase again:
Your identification has been saved in /Users/mac/.ssh/id_rsa_guthub.
Your public key has been saved in /Users/mac/.ssh/id_rsa_guthub.pub.
The key fingerprint is:
SHA256:RGjx8s0FgkwPh+yuCyu5w1uQ+K08DNqGXt/mJWwvliE 1592096012@qq.com
The key's randomart image is:
+---[RSA 2048]----+
|     ++=+ .      |
|      B* . .     |
|     o. +   .    |
|. .   .+ o .     |
|.o   .  S o      |
|.... Eo.         |
|o*oo...+o.       |
|*oB+o o=+        |
|oB=..o+o..       |
+----[SHA256]-----+

```

```
.ssh ls
id_rsa            id_rsa.pub        id_rsa_github     id_rsa_github.pub
➜  .ssh cat id_rsa_guthub.pub  //查看密钥
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDS+udtGpVURtYW8A2XLGVaXh/7MD23wnC5s1xO5bVn0yFzvwy9UattxH9DfXBHg0IbPEgtMTV98PHydsiVUFK1q5KR4PzqKg/+v2HZSuhHwetMz337Ym0itbUXLiaiUiRcZ509LLZDAuzoCZ89UHp+G+Gu7yoXzWBcD8eR7sz6ipj89+lxYX/KucUDqnhbS64EYrFSqMH2PZaKyfXOg9vLTSDy6S1hr/9CPDXrbPVg4e5P5ce2TxcyzOCjdWWAFAOL+IAvaH3wG2fOoxHvklvv/hI3DlEkAcUmTNBA+spgWZlICa6alZ0zXZ8tcIwEKFEz5yZ1lrf0CkerPaKeYe05 1592096012@qq.com


.ssh mkfile -n m config  //添加配置文件



  1 Host showgold.cn
  2    HostName showgold.cn
  3    IdentityFile  ~/.ssh/id_rsa
  4
  5 Host github.com
  6    HostName github.com
  7   IdentityFile  ~/.ssh/id_rsa_guthub

vim config (进行读写配置文件)

```
