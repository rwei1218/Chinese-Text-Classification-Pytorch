# 从零开始训练文本分类模型

## （一）安装Anaconda环境
Anaconda 是一个用于科学计算的 Python 发行版，支持 Linux, Mac, Windows, 包含了众多流行的科学计算、数据分析的 Python 包，是我们运行各类 Python 代码的基础环境。
* **第1步**: 下载Anaconda安装包。[下载链接](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-5.3.1-MacOSX-x86_64.pkg)；
* **第2步**: 双击pkg安装文件，安装Anaconda，[参考链接](https://www.csdn.net/tags/Mtjagg4sNTMzNjctYmxvZwO0O0OO0O0O.html)（执行至参考链接步骤五）。此时打开cmd，命令行输入`conda info -e`，若正常显示conda environments，则第2步成功。若显示无此命令，则需要配置conda环境变量，[参考链接](http://t.zoukankan.com/wangdaodao-p-8124162.html)；
* **第3步**: 为Anaconda设置国内下载源（对抗GFW），打开cmd，输入`vim .condarc`编辑`.condarc`文件，[参考链接](https://mirror.tuna.tsinghua.edu.cn/help/anaconda/)；
* **第4步**: 1）创建虚拟 Python 环境，打开cmd，输入`conda create -n py36 python=3.6`命令，按提示选择`y`；2）激活 Python 环境，打开cmd，输入`conda activate py36`；3）为pip设置国内下载源（对抗GFW），输入`pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`;
## （二）安装本项目依赖库
* **第1步**: 下载本项目代码。[下载链接](https://codeload.github.com/rwei1218/Chinese-Text-Classification-Pytorch/zip/refs/heads/master)
* **第2步**: 1）打开cmd，进入该文件夹路径；2）输入`conda activate py36`，激活 Python 运行环境；3）安装本项目依赖包，`pip install -r requirements.txt`;
## （三）训练你的第一个文本分类模型
```# 训练并测试：
# TextCNN
python run.py --model TextCNN --embedding random

# TextRNN
python run.py --model TextRNN --embedding random

# TextRNN_Att
python run.py --model TextRNN_Att --embedding random

# TextRCNN
python run.py --model TextRCNN --embedding random

# FastText, embedding层是随机初始化的
python run.py --model FastText --embedding random 

# DPCNN
python run.py --model DPCNN --embedding random

# Transformer
python run.py --model Transformer --embedding random
```