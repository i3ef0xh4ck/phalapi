![apic](http://webtools.qiniudn.com/master-LOGO-20150410_50.jpg)  

# [PhalApi 2.4.2 - 接口，从简单开始！](https://www.phalapi.net/) 

[![Latest Stable Version](https://poser.pugx.org/phalapi/phalapi/v/stable)](https://packagist.org/packages/phalapi/phalapi)
[![Total Downloads](https://poser.pugx.org/phalapi/phalapi/downloads)](https://packagist.org/packages/phalapi/phalapi)
[![Latest Unstable Version](https://poser.pugx.org/phalapi/phalapi/v/unstable)](https://packagist.org/packages/phalapi/phalapi)
[![License](https://poser.pugx.org/phalapi/phalapi/license)](https://packagist.org/packages/phalapi/phalapi)

## 独家赞助商
此版本由[（点击成为）](https://www.phalapi.net/ad.html)独家赞助。  

## 快速安装

### composer一键安装

使用composer创建项目的命令，可实现一键安装。

```bash
$ composer create-project phalapi/phalapi
```
> 温馨提示：关于composer的使用，请参考[Composer 中文网 / Packagist 中国全量镜像](http://www.phpcomposer.com/)。

### 手动下载安装

或者，也可以进行手动安装。将此Git项目代码下载解压后，进行可选的composer更新，即：  
```bash
$ composer update
```

## 调用接口

随后，可通过以下链接，访问默认接口服务，即：```s=App.Site.Index```。  
```
http://localhost/path/to/phalapi/public/
```
> 温馨提示：推荐将访问根路径指向/path/to/phalapi/public。

对应执行的PHP代码在./src/app/Api/Site.php文件，源码片段如下：  
```php
<?php
namespace App\Api;
use PhalApi\Api;

class Site extends Api {
    /**
     * 默认接口服务
     */
    public function index() {
        return array(
            'title' => 'Hello ' . $this->username,
            'version' => PHALAPI_VERSION,
            'time' => $_SERVER['REQUEST_TIME'],
        );
    }
}
```

接口请求后结果输出类似如下：  
```
{
    "ret": 200,
    "data": {
        "title": "Hello PhalApi",
        "version": "2.4.2",
        "time": 1501079142
    },
    "msg": ""
}
```

运行效果，截图如下：  

![20170726223129_eecf3d78826c5841020364c852c35156](https://user-images.githubusercontent.com/12585518/52100580-09133a80-2613-11e9-9854-e11c7e789646.jpg)

## 文档
更多请查看：[PhalApi 2.x 开发文档](http://docs.phalapi.net/#/v2.0/)。  

## PhalApi官方创新项目

 + [小白接口](https://www.okayapi.com/?f=github)

## 有问题，怎么办？  

如发现问题，或者任何问题，欢迎提交Issue到[这里](https://github.com/phalapi/phalapi/issues)，或进入[PhalApi开源社区](http://qa.phalapi.net/?f=github)。
