# qrcode_song
自己做的一个小工具，基于Python3.5,requests,beautifulsoup(bs4),草料二维码API的二维码生成器。<br>

##样例（在test.py中也有）：<br>
```Python
from qrcode import qrcode_text_link
from qrcode import qrcode_text_png
from qrcode import qrcode_link_link
from qrcode import qrcode_link_png

print(qrcode_text_link('abc'))
# qrcode_text_link函数可以返回参数文本的二维码网页链接（访问该网页就可以看到二维码图片）

qrcode_text_png('abc',1)
# qrcode_text_png函数可以把文本的二维码保存到本地，传入非零mode参数可以启用美化模式，另外还有两个参数filepath和filename，默认值分别为'./'和'qrcode_song.png'

print(qrcode_link_link('www.baidu.com'))
# qrcode_link_link函数可以返回参数网址的二维码网页链接（不需要加http://或者https://）

qrcode_link_png('www.baidu.com')
# qrcode_link_png可以把链接的二维码保存到本地，另外还有两个参数同上
```

<br>注：以上功能需要在联网的条件下实现。（因为基于网页爬虫）
