## 打卡方法

1. 创建打卡的目录
2. 编写 check-in.md
3. 如果有自己的打卡方法，可以在自己的打卡目录单独创建一个 README 进行补充说明
4. 写好后建议使用 lint-md 进行中文 markdown 语法检查后再推送

## 参考打卡模板

二级目录为时间，三级目录可自行定义

```markdown

## 2024-08-05 11:06:02 星期一

### 计划

- [x] 创建一个学习项目
- [ ] 阅读 Laravel 源码

### 遇到的问题

- PHP 命名空间和 Java import 的区别

### 总结

- 了解了 PHP Composer 的基本原理

```

## markdown 语法检查

```bash

npm install -g @lint-md/cli

# check
lint-md you-path/**.md

# fix
lint-md you-path/**.md --fix

```
