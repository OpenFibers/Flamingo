## Flamingo - 牛逼的键盘映射、宏定义、脚本热键工具，支持 macOS Sierra 10.12，替代Karabiner

Flamingo 不仅是个键盘映射工具，还支持宏定义，和一键执行 shell 脚本。  

[For English Introduction, Click Here](https://openfibers.github.io/flamingo)

### [下载 1.0.0](https://github.com/OpenFibers/flamingo/raw/master/Apps/Flamingo.app_1.0.0.zip)

### 按键映射
举个栗子，比如想要映射鼠标中键为Mission Control，打开Flamingo的Preferences，配置如下设置（配置为JSON格式）:  
```
{
  "map" : [
    {
      "from" : "mouse2",
      "to" : "control up"
    }
  ]
}
```

### 按键宏定义
简单来说就是按一个键，Flamingo帮你按一串按键。  
比如一键自动写行代码什么的：  
<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/autotype.gif" alt="auto_type" style="width: 430px;"/>

在Preferences中配置如下：

```
{
  "map" : [
    {
      "alias" : "Create New Object",
      "from" : "option ]",
      "to" : "[ [ space a l l o c ] space i n i t ] ; left left left left left left left left left left left left left left "
    }
  ]
}
```

也可以一键大招什么的：  
![](https://github.com/OpenFibers/flamingo/raw/master/Images/dota2_kael.gif)

### 脚本热键

举个栗子：按 control + escape，一键唤起 Terminal 并切到工程路径，更新git：  

```
{
  "map" : [
    {
      "from" : "control escape",
      "script" : "cd ~/projects/flamingo&&git pull"
    }
  ]
}
```

[完整用法和全部按键定义请戳我](https://openfibers.github.io/flamingo/help_cn)

### 无法映射按键？将Flamingo添加到辅助功能
1. 打开系统偏好设置 App
2. 打开 "安全性与隐私 -> 隐私 -> 辅助功能"  
3. 添加 Flamingo.app 到右侧列表中  
* 即使不加到辅助功能中，也可以映射鼠标到键盘按键。  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/privacy_cn.png" alt="privacy_cn" style="width: 668px;"/>

### 安全性
没网络连接，也不打log，你懂的。放心用。  
但是千万别从别的地方下载本软件，软件被黑客改过又加监控键盘权限是很危险的。  
如果怀疑Flamingo盗取按键信息，呃，你可以报警，让警察来抓我：）  

### 免费版本与付费版本的区别
免费版支持不限数量的配置文件，每个配置文件最多包含六条配置。付费版无任何限制。  
[点我花30块钱成为作者跪舔的尊贵付费用户](https://openfibers.github.io/flamingo/purchase).  

[For English Introduction, Click Here](https://openfibers.github.io/flamingo)

### [下载 1.0.0](https://github.com/OpenFibers/flamingo/raw/master/Apps/Flamingo.app_1.0.0.zip)

使用有问题？发邮件到 [openfibers@gmail.com](mailto://openfibers@gmail.com).  
