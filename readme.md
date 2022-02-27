# 主要参考文件
https://igloo302.github.io/2020/30%E5%88%86%E9%92%9F%E5%BB%BA%E7%AB%8B%E4%B8%80%E4%B8%AA%E4%BD%9C%E5%93%81%E9%9B%86%E7%BD%91%E7%AB%99-powered-by-hugo/

# 配置SSH
在public文件夹下打开git bash

先确认已登录用户名和邮箱

    ssh-keygen -t rsa -b 4096 -C "邮箱"

随便取个名字，比如1

    Enter file in which to save the key (C:\Users\MSIK/.ssh/id_rsa): 1

在github个人profile的setting的ssh中配置这个生成的1文件（new一个ssh key复制粘贴）

确认ssh-agent在运行中

    eval "$(ssh-agent -s)"

添加

    ssh-add 1

尝试连接github

    ssh -T git@github.com


# git推送
在public文件夹下打开git bash

第一步

    git add .

第二步

    git commit

或者

    git commit -m "版本名字"

第三步

    git push -u origin master