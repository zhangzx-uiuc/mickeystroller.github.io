---
layout: post
title: Lab-1 of Distributed Programming
---

Project Goal
---
This project is about using hdfs to store video data. 


Install Hadoop
---
I referred to [1][2] for installation of Hadoop.

Casting video and receiving data stream
---
The casting step is discussed on page 56 of [3]. I manually casted the video located at "/home/hadoop/Desktop/lab-1/demo.mp4" and sent streams to "rtp://239.1.1.1:5004".

The code of receiving stream is shown below:
{% highlight java %}
String command_vlc_receive[]={"/bin/sh","-c","vlc -vvv rtp://239.1.1.1:5004 --sout file/ts:/home/hadoop/Desktop/lab-1/stream.mp4"};
Runtime.getRuntime().exec(command_vlc_receive).waitFor();
{% endhighlight %}

Notice the ".waitFor()" at the end of the second line. This method allows us to receive all streams before uploading the video to hdfs.

Upload video to HDFS
---
Most of codes are provided on page 57 of [4]. 


Reference:
---
1. [Hadoop安装教程_单机/伪分布式配置](http://dblab.xmu.edu.cn/blog/install-hadoop/)
2. [使用Eclipse编译运行MapReduce程序](http://dblab.xmu.edu.cn/blog/hadoop-build-project-using-eclipse/)
3. [实战hadoop:开启通向云计算的捷径(作者刘鹏)](http://www.linuxidc.com/Linux/2013-05/85132.htm)
4. [Using VLC to send&recieve video streams](https://www.videolan.org/doc/streaming-howto/en)