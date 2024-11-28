base环境下

```
D:\Config\anaconda3\lib\pythonx.x\site-packages
```

虚拟环境下

```
D:\Config\anaconda3\envs\xxxx\Lib\\site-packages
```



新建`sitecustomize.py`文件，复制以下代码：

```
import sys
from IPython.core.ultratb import ColorTB
 
sys.excepthook = ColorTB()
```

然后安装库，`pip install IPython`