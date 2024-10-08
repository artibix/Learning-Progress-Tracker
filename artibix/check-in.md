## 2024-09-12

### Reading

- 什么是 i18n：国际化（internationalization）的缩写，指软件为多个地区和文化提供的支持。
- PyPy 和 CPython 的区别：实现上的区别；PyPy 启动慢，执行快，CPython 启动快，执行慢；PyPy 对 C 扩展兼容性不好...（关于 PyPy 的实现过程可以参考「自举」）
- 自举：汇编写的简单的 C 编译器，再利用这个 C 编译器写 GCC，GCC 又来编译 C。（计算机历史上的自举过程数不胜数）

## 2024-09-11

### Reading

- 微信公众号（PHP 自学中心）：`kill -9` 强制停止程序， `kill -15` 请求程序结束

### Laravel Source Code

- `static::` 是 PHP 的后期静态绑定机制，确保在继承层次中调用的静态方法或属性是实际调用类的版本，而不是定义这个方法的类。
- Facade 本质上是一个代理，它为服务容器中的类提供了一个静态接口。在后台，Facade 通过服务容器解析出具体的类实例并调用其方法。（不需要手动注入或解析服务实例）
- 工厂模式：将所有依赖放在工厂里面，使用这些依赖仅需依赖工厂。
- DI：只要不是由内部生产（比如初始化、构造函数 __construct 中通过工厂方法、自行手动 new 的），而是由外部以参数或其他形式注入的，都属于 依赖注入（DI）

```php
$superModule = new XPower;

$superMan = new Superman($superModule);
```

- IoC：控制反转的核心思想是将对象创建和依赖关系的控制从对象自身转移到外部系统。`container` 通过 `bind` 和 `make` 将所有依赖解耦。

## 2024-09-10

### Laravel Source Code

- Q: PSR-4 的顶级命名空间是什么？
- A：主要用于将逻辑上不同的部分映射到不同的物理目录，从而实现自动加载。

```json
{
    "autoload": {
        "psr-4": {
            "App\\": "src/App/",
            "Vendor\\": "src/Vendor/"
        }
    }
}
```
- Q: 为什么 composer.json 里面的命名空间是双反斜杠？
- A: 在 json 里面，单反斜杠会转义。
- Composer 的初始化与注册。初始化负责顶层命名空间的目录映射，注册负责实现顶层以下的命名空间映射规则。
- Q: 为什么静态导入使用 **hash->path** 键值对
- A: 1. 防止冲突。2.优化加载性能（require 导入）。3. 对文件进行版本控制。

### Reading

- RuanYiFeng: 订阅制（前期实惠，后面涨价）能够减少二手市场的冲击
- RuanYiFeng：团队越大，越需要文档，避免 **隐形知识**

## 2024-09-04

### LeetCode

- 刚开始接触滑动指针还是烧脑

### [OAuth 2.0](https://www.ruanyifeng.com/blog/2014/05/oauth_2_0.html)

- 简单化理论：在小区授权给外卖小哥临时门禁密码

- 四种授权方式的区别
	1. 授权码适合前后端分离项目；
	2. 隐藏式：适合纯前端项目；
	3. 密码式：直接给用户密码；
	4. 凭证式：无前端项目。

### Laravel 源码

- `__autoload (PHP 5, now deprecated)` 和 `spl_autoload` 的区别：前者单一，后者灵活，兼容性强。
- PSR-0 & PSR-4 标准


## 2024-08-05 19:06:02 星期一

### 计划

- [x] 创建一个学习项目
- [x] 阅读 Laravel 源码
- [x] 看两节 TED 英语动画
- [x] 刷 leetcode
- [x] 看《社会心理学》
- [x] 运动一小时

### 问题

- PHP 命名空间和 Java import 的区别

### 总结

#### 算法

- python `list.count` 会遍历 list，有一层 O(n) 的复杂度

#### PHP Composer 导包的原理

- 略

#### 社会心理学第一编第一章

- 一个了解自我的视角（但不是唯一）
- 研究人们如何看待彼此
- 研究的问题：人们如何构筑世界？社会直觉如何引导我们的行为？我们的行为如何被环境/人影响的？
- 是一门关于环境的学科
- 人总是被自身的价值观影响
- 理论用来总结事实

#### Learn and more

-  The Man Who Could Sit Anywhere: comfortable, radioactive.
- I Save My Dog From Death: forbade(forbid v2), weeping(weep v-ing), basement, puppy, cruel, threw，immediately, persuade, kept(keep v2,v3), scare, tuck, shiver, hurried(hurry v2,v3), shed, hid(hide v2), snuck(sneak v2,v3), blanket, bowl, pet, breed, clumsily, bark, shelter, toy, squeaky, frog, menace, insane, infect, tears, furious, wiggle.