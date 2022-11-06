Git 全局配置用户名、邮箱

```shell
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```



Git 记住当前账户密码

（1）如果密码更新，则需要重新输入一次正确的密码，后续会以新的正确的密码为准；

```shell
git config --global credential.helper store
```



Git 查看全局配置

（1）通过用户目录 .gitconfig 文件查看

```shell
# Windows 环境使用 git bash
cat /c/Users/user/.gitconfig

# Linux 环境
cat ~/.gitconfig
```

（2）通过命令行查看

```shell
git config --list
```



---



```shell
# Windows 环境 Git 配置
safe.directory=*
```

当 Windows 系统更新 Git 版本后，总是会提示如下错误，导致 Windows 中的 Git 无法正常使用

![image-20221106172254433](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20221106172301.png)

此时将 Windows 环境下的 Git 进行如下配置即可

```shell
git config --global --add safe.directory '*'
```



