本地搭建环境:
Apache2.4.39+php7.4.3+mysql5.7.26

系统版本为：HadSky v7.12.10

在后台上传应用功能里，未对zip压缩包进行过滤。 
先写一个一句话木马。
然后压缩该文件。
在后台该位置上传：/index.php?c=app&a=superadmin

![image](https://github.com/fenglon/CVE/assets/94779688/206db9e2-d666-4339-b383-6d5c70054aa8)

上传压缩包。

![image](https://github.com/fenglon/CVE/assets/94779688/3f5ba66e-bd55-4467-a872-32d1a4963f5e)

分析代码发现解压文件被解压到初始页面下，直接访问即可。

![image](https://github.com/fenglon/CVE/assets/94779688/e1fba321-2560-4f0f-a68e-59a8892d4842)

压缩包被自动解压。
木马写入成功。

![image](https://github.com/fenglon/CVE/assets/94779688/b1772d2c-7540-49ad-a84f-5a158f014bb0)

