# VPS-bilibili
根据辰旭大佬项目修改，源地址：https://github.com/chenxuuu/24h-raspberry-live-on-bilibili 他的直播间：http://live.bilibili.com/16703
原项目是供树莓派使用的，然后我突发奇想能不能在VPS上运行呢，于是就研究了一下
主要的问题是树莓派可以使用h264_omx编码器，而VPS连显卡都没有，所以一开始玩的时候根本无法推流
后来把play.py文件中的推流参数h264_omx改为libx264就可以用了，然后要是推流文字想显示其他内容可以修改default_ass.py文件，!注意，请保留树莓派项目源地址!！
先写这么多，之后慢慢补充，安装过程基本参考原项目就可以了，主要是在安装x264编码器时和ffmpeg时把与树莓派相关的参数删掉就可以了
