# GenshinWishCalculator


## 功能介绍
>本插件可以根据玩家当前拥有纠缠之缘数目和角色池、武器池的水位、保底情况，计算出抽取指定数目五星up角色和特定的五星up武器的概率

>使用本插件需要python环境和numpy库，如果觉得不方便，你还可以使用[纯js版本](https://github.com/MSIsunny/GenshinWishCalculator),但是运行的速度将会大大降低

## 安装教程

>以下教程均基于windows系统，未验证其他系统的可行性，其他系统的使用者请尝试自行安装python环境和numpy库

1、安装python环境，如果已经有python环境，可以直接看步骤2


>教程使用的python版本为3.9.0，这里我们使用华为源下载：[64位win版下载链接](https://mirrors.huaweicloud.com/python/3.9.0/python-3.9.0-amd64.exe)

>下载完后直接安装，但是注意：安装时请勾选“Add Python 3.9 to PATH”选项，否则无法在cmd中使用python命令，并且请选择默认安装pip，以方便接下来安装numpy库

2、安装numpy库，如果已经有numpy库，可以直接看步骤3

>打开cmd或powershell，输入以下命令安装numpy库(清华源)

```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple numpy
```
>安装完成后，重启你的电脑或服务器

3、自行将本项目clone到本地或服务器，或者直接下载zip包

>将WishCalculatorViaPy.js和WishSupport.py两个文件都放到云崽的example文件夹下，启动云崽即可使用

## 使用教程

>在群里发送  计算/概率/期望 任一关键词即可查看使用帮助，内有详细使用教程

<img width="350" src="https://github.com/MSIsunny/GenshinWishCalculator-py/blob/main/image/help.jpeg"> </img>

>按照顺序提供数据即可以计算达到抽卡预期的概率

<img width="350" src="https://github.com/MSIsunny/GenshinWishCalculator-py/blob/main/image/usage.jpeg"> </img>

>注意：因为本插件的计算量比较大，为避免被用户滥用，默认不支持私聊，仅支持群聊使用

## 已知问题

>如果在终端中输入代码```python```出现诸如command not found: python之类的提示，但是输入代码```python3```可以正常进入python命令行交互模式

>那么，请将WishCalculatorViaPy.js文件中85行附近的一处python改为python3

## 实现原理

>使用转移概率矩阵计算祈愿概率，与迭代法模拟上万次抽卡不同，此方法得到的是精确结果，不存在随机涨落

>计算结果的正确性已经通过迭代法大量模拟抽卡得到初步验证，如果仍存在错误还望指出

