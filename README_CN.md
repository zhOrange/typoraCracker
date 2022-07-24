# typora Cracker

一个typora的Patch和KeyGen工具

## 敬告
```
仅供学习和讨论，请不要从事任何非法行为。
由此产生的任何问题都将由用户（您）承担。
```

## Features

- 理论上支持Typora支持的所有操作系统

## 食用方式

1. `pip install -r requirements.txt`
2. `python typroa.py --help`
3. 阅读帮助文档及使用。
4. 修改导出的 License.js。
5. 替换原目录下的 app.asar。
6. 运行KeyGen程序。
7. 正常激活。


## 示例

```shell
> python typroa.py --help
usage: typora.py [-h] [-u] [-f] asarPath dirPath

[extract and decryption / pack and encryption] app.asar file from [Typora].

positional arguments:
  asarPath    app.asar file path/dir [input/ouput]
  dirPath     as tmp and out directory.

optional arguments:
  -h, --help  show this help message and exit
  -u          pack & encryption (default: extract & decryption)
  -f          enabled prettify/compress (default: disabled)

If you have any questions, please contact [ MasonShi@88.com ]

> python typora.py {installRoot}/Typora/resources/app.asar workstation/outfile/
⋯
> python typora.py -u workstation/outfile/ workstation/outappasar
⋯
> cp {installRoot}/Typora/resources/app.asar {installRoot}/Typora/resources/app.asar.bak
> mv workstation/outappasar/app.asar {installRoot}/Typora/resources/app.asar
# (patch code)
> node keygen.js
XXXXXX-XXXXXX-XXXXXX-XXXXXX
> typora
# (input info)
email: crack@example.com
serial: XXXXXX-XXXXXX-XXXXXX-XXXXXX
```

## LICENSE
 MIT LICENSE


 ## for beta version

 ### Typora

> 对于现在的新版本，我觉得也没必要破解，作者并没有把以前的版本也收费，已经对他来说仁至义尽了，但是令人琢磨不懂的是，老版本会有过期问题。

放了两个老版本版本的Typora，都是以前的免费版，但是会过期，本项目旨在解决过期问题。

```
链接：https://pan.baidu.com/s/1JBCMcUzs9BH-5nYVCCIiTQ?pwd=5maz 
提取码：5maz
```

### typora Cracker

原项目是[fossabot/typoraCracker: A patch and keygen tools for typora. (github.com)](https://github.com/fossabot/typoraCracker)的，我拿过来使用，防止后面Typora不给用了，我有个备份。

本项目里面的dec_app是已经修改过的了，所以直接放到Typora下改名为`app`就可以用。

下面是解决步骤。

**遇到Typora过期问题**

```
This beta version of Typora is expired, please download and install a newer version.
```
解决方案如下：

1、下载解密typoraCracker教程

https://github.com/fossabot/typoraCracker 

> 现在我们这个项目里面就可以用了，下面操作都不需要。

下载后，win+R打开cmd，进入typoraCracker目录。

2、执行命令
```
pip install -r requirements.txt
python typora.py "C:\Program Files\Typora\resources\app.asar" .  // 你Typora安装在那个文件夹下面就是那个文件夹
```
会在 typoraCracker 文件夹下生成dec_app文件
3、修改我们反编译的 dec_app 文件夹下的 `License.js`文件

我们省事，直接将文件中`1636297098336`全部替换成`4713176400336`
这就是修改注册时间，如果想研究一下源码也是可以的。
好了，这个时候我们保存这个文件

>如果搜索不到上面两个数字，就尝试搜搜'getTime'方法，看附近有没有。或者直接以文档中的License.js替换。

4、文件替换

把dec_app，把它复制到Typora目录下的resources，并改名为app
现在我再打开typora就可以使用了。

