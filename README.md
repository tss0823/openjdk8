## 当前环境

1. mac 10.13.2
2. 系统已经安装了jdk "1.8.0_151"

##依赖软件
- Xcode
- llvm  
```
sudo ln -s /usr/bin/llvm-g++ /Applications/Xcode.app/Contents/Developer/usr/bin/llvm-g++  
sudo ln -s /usr/bin/llvm-gcc /Applications/Xcode.app/Contents/Developer/usr/bin/llvm-gcc 
```
- freetype
- XQuartz


## 编译步骤
1. hg clone http://hg.openjdk.java.net/jdk8/jdk8 jdk8
2. cd jdk8 && source .bash_porfile
2. cd jkd8 && get_source.sh --with-debug-level=slowdebug --with-target-bits=64
3. make all 2>& 1 | tee abc.txt
```
第二步如果错误，请检查环境配置，
.bash_profile为环境变量先关配置
--with-debug-level=slowdebug 表示编译出详细的调试信息
```

## 参考文献
> http://jimmee.iteye.com/blog/2288307
> https://github.com/ydcun/Java/blob/master/java/src/main/java/com/ydcun/openjdk/jdk8/MAC%E7%BC%96%E8%AF%91OpenJDK8.md
