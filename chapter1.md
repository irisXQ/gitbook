\# 1. 确定java环境：

\`\`\`

    \# java -version

\`\`\`

\# 2. 下载eclipse for linux 的安装包

\`\`\`

\# 方法一： 直接在终端下载

    \# wget http://ftp.kaist.ac.kr/eclipse/technology/epp/downloads/release/luna/SR2/eclipse-java-luna-SR2-linux-gtk-x86\_64.tar.gz



\# 方法二： 复制下载链接到迅雷下载，然后copy到share folder中

\`\`\`

\# 3. 解压

\`\`\`

\# 指定解压到/opt目录下

    \# tar -zxvf eclipse-\*.tar.gz -C /opt 

\`\`\`

\# 4. 创建源链接

\`\`\`

    \# ln -s /opt/eclipse/eclipse /usr/share/eclipse

\`\`\`

\# 5. 创建桌面快捷方式

\`\`\`

    \# cd /usr/share/applications

    \# vim eclipse.desktop

\# 插入如下代码：

    \[Desktop Entry\]

    Encoding=UTF-8

    Name=Eclipse 4.4.1

    Comment=Eclipse Luna

    Exec=/usr/bin/eclipse

    Icon=/opt/eclipse/icon.xpm

    Categories=Application;Development;Java;IDE

    Version=1.0

    Type=Application

    Terminal=0

\`\`\`

\# 6. 查看应用程序中是否已经添加了 编程-&gt; eclipse 的选项



\# 7. 打开eclipse，开始使用

