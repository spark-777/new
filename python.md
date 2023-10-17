

# git

### 网络问题

clash

`	git config --global http.https://github.com.proxy http://127.0.0.1:7890`

wsl动态

`	PROXY_HTTP="http://${204.13.153.220}:${80}"`

`	git config --global http.https://github.com.proxy ${PROXY_HTTP}`

`	git config --global http.https://github.com.proxy "http://${204.13.153.220}:${80}"`



克隆仓库,将GitHub上的仓库克隆到本地计算机

`	git clone <仓库URL>`

**添加文件：** 将项目文件添加到本地仓库,文件需要在仓库文件夹内

`	git add <文件名>`

**提交更改：** 将添加的文件或修改提交到本地仓库。

`	git commit -m "提交消息"`

**推送更改：** 将本地提交的更改推送到GitHub仓库。

`	git push origin <分支名>`





# python



### 获得当前目录下所有文件

```
import os
for root, dirs, files in os.walk(".", topdown=False):
    for name in files:
        print(os.path.join(root, name))
```





### BeautifulSoup

创建BeautifulSoup对象

```
html_doc = """
<html><head><title>The Dormouse's story</title></head>
<body>
<p class="title"><b>The Dormouse's story</b></p>

<p class="story">Once upon a time there were three little sisters; and their names were
<a href="http://example.com/elsie" class="sister" id="link1">Elsie</a>,
<a href="http://example.com/lacie" class="sister" id="link2">Lacie</a> and
<a href="http://example.com/tillie" class="sister" id="link3">Tillie</a>;
and they lived at the bottom of a well.</p>

<p class="story">...</p>
"""


from bs4 import BeautifulSoup
soup = BeautifulSoup(html_doc, 'html.parser')
```



```
soup.find_all('div', {'data-power': '电动'})
```

```html
<div class="col-xs-6 col-sm-3 set-col" data-item="thumbnail" data-tons="剪叉式" data-power="电动" data-emissions=""
    data-tag="自行剪叉式高空作业平台">
    <div class="thumbnail">
        <a href="https://www.liugong.com/product/lsc0407dem/" title="LSC0407DEM" target="_self"><img
                src="http://www.liugong.com/wp-content/uploads/2023/08/LSC0407DEM-530-370.png" width="100%"
                alt="LSC0407DEM">
        </a>
    </div>
</div>
<div class="col-xs-6 col-sm-3 set-col" data-item="thumbnail" data-tons="剪叉式" data-power="电动" data-emissions=""
    data-tag="自行剪叉式高空作业平台">
    <div class="thumbnail">
        <a href="https://www.liugong.com/product/lsc0507dem/" title="LSC0507DEM" target="_self"><img
                src="http://www.liugong.com/wp-content/uploads/2023/08/LSC0507DEM-530-370.png" width="100%"
                alt="LSC0507DEM">
        </a>
    </div>
</div>
```

```
#上述为a的值，a为find_all的返回值
len(a) = 2
a[0]["data-tag"] = 自行剪叉式高空作业平台
a[0].a["href"] = "https://www.liugong.com/product/lsc0407dem/"
a[0].img['alt'] = 'LSC1012DH'
```







### requests

```
import requests

url = 'http://mall.sany.com.cn/new/list/?cat_id=329'
headers = {"User-Agent": "Mozilla/5.0 (iPhone; CPU iPhone OS 11_0 like Mac OS X) AppleWebKit/604.1.38 (KHTML, like Gecko) Version/11.0 Mobile/15A372 Safari/604.1",
           "Content - Type": "application/x-www-form-urlencoded; charset=UTF-8",
           "Referer": "https://fanyi.baidu.com/?aldtype=16047",
           "Accept - Encoding": "gzip, deflate, br",
           "Accept - Language": "zh-CN,zh;q=0.9"}
response = requests.get(url, headers=headers)
#解决乱码问题
response.encoding = response.apparent_encoding
print(response.text)
```













### conda

```
conda create -n name python=3.7.3
```

```
conda activate rnaseq
```

```
conda deactivate
```



###  matplotlib

导入并解决中文乱码

```
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif'] = ['SimHei'] #用来正常显示中文标签
plt.rcParams['axes.unicode_minus'] = False #用来正常显示负号
```
绘制环形图

```
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif'] = ['SimHei'] #用来正常显示中文标签
plt.rcParams['axes.unicode_minus'] = False #用来正常显示负号
my_dpi=96
plt.figure(figsize=(480/my_dpi,480/my_dpi),dpi=my_dpi)
plt.pie(x=[7,13],
        labels=['没有储能系统和ems的公司','有储能系统和ems的公司'],
        wedgeprops={'width':0.3},#空心部分大小参数
        colors=["#d5695d", "#5d8ca8"], 
        explode=(0, 0.01),#某部分突出显示，值越大，距离中心越远，该法可解决饼图字体重叠的问题
       )
plt.savefig('r.png')
plt.show()
```



### panda

```
import pandas as pd
#禁用科学记数法
pd.set_option('display.float_format', lambda x: '%.3f' % x)

```

导入表格

```
data = pd.read_excel('2.xls',header = 1,sheet_name = 1)
#读取文件 header 选择文件的第几行作为标题 默认0
#如果没有标题header = None
Sheet_name  #指定要从excel中读取哪个表格的数据
```



将表格里的NAN值填充为0

```
data = data.fillna(0)
```



### 写入excel

```
from openpyxl import Workbook
# 创建一个 workbook
wb = Workbook()
# 获取被激活的 worksheet
ws = wb.active


for i in range(len(ddd)):
    productName = ddd[i]["data-tag"]
    productUrl = ddd[i].a["href"]
    productNo = ddd[i].img['alt']

    ws.cell(row=i+1, column=1).value=productName
    ws.cell(row=i+1, column=2).value=productNo
    ws.cell(row=i+1, column=3).value=productUrl
    print(productName,productNo,productUrl)


# 保存 Excel 文件
wb.save("sample.xlsx")
```



panda

```
import pandas as pd

# 创建一个包含数据的字典
data = {
    'Term': [
        'AC', 'AWG', 'BMS', 'CAN', 'CEC', 'CE', 'DC', 'DSP', 'ELV', 'EMI',
        'EMC', 'EMS', 'ETL', 'HV', 'HW', 'IP', 'KW', 'LED', 'LV', 'MCU',
        'MTBF', 'PC', 'PFC', 'PF', 'RoHS', 'REACH', 'SW', 'USB'
    ],
    'Definition': [
        'Alternating Current', 'American Wire Gauge', 'Battery Management System',
        'Controller Area Network', 'California Energy Commission', 'European Conformity',
        'Direct Current', 'Digital Signal Processor', 'Extra Low Voltage',
        'Electromagnetic Interference', 'Electromagnetic Compatibility',
        'Electromagnetic Susceptibility', 'Electrical Testing Laboratories',
        'High Voltage', 'Hardware', 'Ingress Protection', 'Kilowatt',
        'Light Emitting Diode', 'Low Voltage', 'Microcontroller',
        'Mean Time Between Failure', 'Personal Computer', 'Power Factor Correction',
        'Power Factor', 'Restriction of Hazardous Substances',
        'Registration, Evaluation, Authorization and Restriction of Chemicals',
        'Software', 'Universal Serial Bus'
    ]
}

# 创建一个DataFrame
df = pd.DataFrame(data)

# 将DataFrame写入Excel文件
excel_file = 'terms.xlsx'
df.to_excel(excel_file, index=False)

print(f'Data has been written to {excel_file}')
```





批量修改文件名

```python
import os,sys                       #导入模块
def add_prefix_files():             #定义函数名称
    i = 1
    mark = 'test-'                 #准备添加的前缀内容
    old_names = os.listdir()  #取路径下的文件名，生成列表
    for old_name in old_names:      #遍历列表下的文件名
            if  old_name!= sys.argv[0]:  #代码本身文件路径，防止脚本文件放在path路径下时，被一起重命名
               if old_name.endswith('.iso'):   #当文件名以.txt后缀结尾时
                    os.rename(os.path.join(old_name),os.path.join(str(i)+".mp4"))  #重命名文件
                    i = i+1
                    print (old_name,"has been renamed successfully! New name is: ",mark)  #输出提示

if __name__ == '__main__': 
        # path = r'E:\我的学习\编程\Python\PythonTest2\Test2'   #运行程序前，记得修改主文件夹路径！
        add_prefix_files()         #调用定义的函数，注意名称与定义的函数名一致
        print("----")

```











# linux

创建文件夹

```
mkdir
```



### vim

```
:w 保存文件但不退出vi
:w! 强制保存，不退出vi
:wq 保存文件并退出vi
:q 不保存文件，退出vi
:q! 不保存文件，强制退出vi
:e!  放弃所有修改，从上次保存文件开始再编辑
```



# 获取cookie

```
2javascript:alert
```

在要获取cookie的网页的地址栏输入，复制过去把2删除，直接复制"javascript"会被过滤



# ffmpeg


ffmpeg切割视频

```
ffmpeg -i 1.mp4 -ss 00:17:50.070 -to 00:21:11.140 -c copy output2.mp4
```

从视频的00：17：50.070剪到00：21：11.140

```
ffmpeg -i 1.mp4 -ss 00:17:50.070 -t 00:21:11.140 -c copy output2.mp4
```

从视频的00：17：50.070开始在添加00：21：11.140时长的内容





# linear regression

## Linear Regression with One Variable

### hypothesis Function

  - $h_{\theta}(x)=\theta_0+\theta_1x$

### Cost Function

  - $J(\theta_0,\theta_1)=\frac{1}{2m}\sum\limits^m_{i=1}(h_{\theta}(x_i)-y_i)^2$

### Gradient Descent

