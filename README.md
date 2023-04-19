# Nps Unauthorized Scan
# 前言
前几日在微信公众号平台看到一篇最近公开nps代理工具0day漏洞的分析，由此利用此原理写了扫描及利用脚本来进行学习，请勿用于非法用途。<br/>
https://mp.weixin.qq.com/s/PTq01wcV4XJwutbSjHjfvA<br/><br/>
该POC会直接输出nps后台的客户端列表及各类隧道列表，单目标检测可以给目标添加一条socket5代理。
# 使用方法
![image](https://user-images.githubusercontent.com/62537001/184465090-b8a86d50-6219-4cb8-8112-1fa87ab52e92.png)
## 单目标检测
python3 npspoc.py -t http://127.0.0.1:8080<br/>
单目标检测会询问是否给需要给指定客户端添加一条socket5代理。
![image](https://user-images.githubusercontent.com/62537001/184465138-467ccf45-c7b6-454d-ac50-ec8d1bc1f040.png)
## 批量检测
python3 npspoc.py -f url.txt</br>
![image](https://user-images.githubusercontent.com/62537001/184465353-d489b61e-284e-4ea4-87e3-b91505a82ffb.png)
## 结果
在result目录下生成ip_端口(127.0.0.1_8080)为名称的txt文档。
![image](https://user-images.githubusercontent.com/62537001/184465421-4a4dd13b-93f9-4d6e-b0a0-65217373c349.png)
##免责申明
由于传播、利用开源信息而造成的任何直接或间接的后果及损失，均由使用者本人负责，作者不承担任何责任。
开源仅作为安全研究之用！切勿用作实战用途！仅限于本地复现！
