# rockchip_rtsp_h264_decode
使用ffmpeg、rkmpp、opencv实现了香橙派Pi5平台的硬件编码

opencv4是修改后的头文件
ffmpeg_rtsp_mpp-master是工程代码，源项目：https://github.com/MUZLATAN/ffmpeg_rtsp_mpp，原作者项目可能已经不维护
请自行接入网络摄像头进行调试，可以使用rtsp标准的网络连接格式，例如：rtsp://admin:Buzhongyao123@192.168.200.228:554/h264/ch39/sub/av_stream
如果用QT编译器打开情况下，会生成CMakeList.txt文件夹，如果这个程序第一次在你的电脑编译时候是没有问题的，那么下次你移动开发环境时候会导致无法正确make，那么请你删除CMakeList.txt.user的文件并且重新编译
Ubuntu22.04 GNOME已经验证可以使用，Ubuntu20.04xfce和Ubuntu22.04xfce未验证

请把opencv4文件夹覆盖到你的/usr/include目录下

建议把工程文件夹下的ffm_lib替换成你自己的依赖文件，原作者的ffmpeg版本比较老了；原作者开发板是firefly所以依赖可能和香橙派不太一样建议把里面的依赖替换成香橙派的。

缺陷报告：目前yuv无法存储，下一个版本争取把yuv生成出来，可以拉取rtsp流
