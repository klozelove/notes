...menustart

 - [Tips](#a0d4cc0f54602c3f247c72f15a7d2dbf)
	 - [符号化crash 日志](#f3339d94a6bf27a7a019412ed2bd3ba9)

...menuend



<h2 id="a0d4cc0f54602c3f247c72f15a7d2dbf"></h2>
# Tips

<h2 id="f3339d94a6bf27a7a019412ed2bd3ba9"></h2>
## 符号化crash 日志

```shell
# ios Debug
export DEVELOPER_DIR="/Applications/Xcode.app/Contents/Developer"
alias symbolicatecrash="/Applications/Xcode.app/Contents/SharedFrameworks/DVTFoundation.framework/Versions/A/Resources/symbolicatecrash"

把你的.crash文件.app文件和.dSYM文件放在同一个目录下然后运行：
symbolicatecrash -v ScaryCrash.crash > Symbolicated.crash
```

## IAP create , app -> ipa

```shell
#!/bin/bash  

APPNAME="justdance"  
ZIPNAME="${APPNAME}zip" 
IPANAME="${APPNAME}IPA" 
  
mkdir -p ./ipa/Payload  
cp -r ./${APPNAME}.app ./ipa/Payload  
cd ipa  
zip -r ${ZIPNAME} *  
mv ${ZIPNAME}.zip ${IPANAME}.ipa  
```
