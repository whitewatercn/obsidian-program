# 初始化

```
git init

```


# 提交
```
git add -A
git commit -m "更新注释"

```

# 远程仓库
## 查看远程库
```
git remote -v
origin	git@github.com:michaelliao/learngit.git (fetch)
origin	git@github.com:michaelliao/learngit.git (push)
```
## 连接远程库
```
git remote add origin 
# 后面加git仓库的ssh链接
```

## 删除
```
git remote rm origin
```

## 推送
1. 普通推送
```
git push -u origin master
```

报错[[Updates were regected]]
2. 强制推送
```
git push -f origin master
```