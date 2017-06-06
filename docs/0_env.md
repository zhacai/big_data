环境配置：
---
1.构建image, `docker build -t hadoop .`

2.运行container，`docker run`

-test 运行测试命令，跑demo MR 程序
docker run --rm --name Hadoop -h hadoop \
    -p 8088:8088 \
    -p 8042:8042 \
    -p 50070:50070 \
    -ti hadoop -test bash

3.看集群情况
Hadoop Browser
http://localhost:8088

http://localhost:50070
HBase Browser
http://localhost:60010
Access by Jupyter Notebook
http://localhost:8888/terminals/1

 sh-4.2# bash <enter>

4.动态配置集群节点