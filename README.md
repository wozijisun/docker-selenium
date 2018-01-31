# docker-selenium
## just for selenium-firefox and chrome container add chinese encode with Dockerfile.

***
Try it.
===
 # docker build -t 172.18.19.189:5000/mts/selenium/node-chrome-debug .
Sending build context to Docker daemon  2.56 kB
Step 1 : FROM selenium/node-chrome-debug
 ---> 7588a4ad0761
Step 2 : MAINTAINER wozijisun
 ---> Running in 343c5786a265
 ---> e2b9ddcd1d7e
Removing intermediate container 343c5786a265
Step 3 : ENV NODE_MAX_INSTANCES 10
 ---> Running in 8d81df557f1e
 ---> 8f0058a23bdd
Removing intermediate container 8d81df557f1e
Step 4 : ENV NODE_MAX_SESSION 10
 ---> Running in 328c562db9d5
 ---> 1d33ab8bbc0d
Removing intermediate container 328c562db9d5
Step 5 : RUN sudo locale-gen zh_CN.UTF-8 && sudo DEBIAN_FRONTEND=noninteractive dpkg-reconfigure locales
 ---> Running in 151c3140503f
Generating locales (this might take a while)...
  zh_CN.UTF-8... done
Generation complete.
Generating locales (this might take a while)...
  en_AG.UTF-8... done
  en_AU.UTF-8... done
  en_BW.UTF-8... done
  en_CA.UTF-8... done
  en_DK.UTF-8... done
  en_GB.UTF-8... done
  en_HK.UTF-8... done
  en_IE.UTF-8... done
  en_IN.UTF-8... done
  en_NG.UTF-8... done
  en_NZ.UTF-8... done
  en_PH.UTF-8... done
  en_SG.UTF-8... done
  en_US.UTF-8... done
  en_ZA.UTF-8... done
  en_ZM.UTF-8... done
  en_ZW.UTF-8... done
  zh_CN.UTF-8... done
Generation complete.
 ---> 24a658a45436
Removing intermediate container 151c3140503f
Step 6 : RUN sudo locale-gen zh_CN.UTF-8
 ---> Running in d618652cb530
Generating locales (this might take a while)...
  zh_CN.UTF-8... done
Generation complete.
 ---> 96e3a1445cb9
Removing intermediate container d618652cb530
Step 7 : ENV LANG zh_CN.UTF-8
 ---> Running in 9f710c547b19
 ---> 03917d83dfcd
Removing intermediate container 9f710c547b19
Step 8 : ENV LANGUAGE zh_CN:zh
 ---> Running in 40c6a34acf19
 ---> 0e5272a2de76
Removing intermediate container 40c6a34acf19
Step 9 : ENV LC_ALL zh_CN.UTF-8
 ---> Running in a90ae70ad024
 ---> 68fe5531c4fb
Removing intermediate container a90ae70ad024
Step 10 : RUN sudo apt-get update -qqy
 ---> Running in ce2a6f0ecdc4
 ---> 4bb4b85d6835
Removing intermediate container ce2a6f0ecdc4
Step 11 : RUN sudo apt-get -qqy --no-install-recommends install     fonts-ipafont-gothic     xfonts-100dpi     xfonts-75dpi     xfonts-cyrillic     xfonts-scalable
 ---> Running in bb1cbdc7b438
 ---> 57b75e0238b3
Removing intermediate container bb1cbdc7b438
Step 12 : RUN sudo apt-get -qqy install ttf-wqy-microhei   && sudo ln /etc/fonts/conf.d/65-wqy-microhei.conf /etc/fonts/conf.d/69-language-selector-zh-cn.conf
 ---> Running in f2ff73709e28
debconf: delaying package configuration, since apt-utils is not installed
正在选中未选择的软件包 fonts-wqy-microhei。
(正在读取数据库 ... 系统当前共安装有 32207 个文件和目录。)
正准备解包 .../fonts-wqy-microhei_0.2.0-beta-2_all.deb  ...
正在解包 fonts-wqy-microhei (0.2.0-beta-2) ...
正在选中未选择的软件包 ttf-wqy-microhei。
正准备解包 .../ttf-wqy-microhei_0.2.0-beta-2_all.deb  ...
正在解包 ttf-wqy-microhei (0.2.0-beta-2) ...
正在处理用于 fontconfig (2.11.94-0ubuntu1.1) 的触发器 ...
正在设置 fonts-wqy-microhei (0.2.0-beta-2) ...
正在设置 ttf-wqy-microhei (0.2.0-beta-2) ...
 ---> 3f4a69d87c1e
Removing intermediate container f2ff73709e28
Successfully built 3f4a69d87c1e
