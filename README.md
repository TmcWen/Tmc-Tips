# Tmc_Wen-Tips
## 这里会写一些我收集来/亲身遇到过的问题解决方案
---
### 自定义再生龙/打包再生龙/打包iso目录为iso文件/Clonezilla zip to iso
### 命令
#### mkisofs -o custom_clonezilla.iso         -b syslinux/isolinux.bin         -c syslinux/boot.cat         -no-emul-boot         -boot-load-size 4         -boot-info-table         -iso-level 3         -J -R -V "CLONEZILLA"        ./
### -o -输出文件名，-b -引导加载器位置，-c -引导目录文件  
---
