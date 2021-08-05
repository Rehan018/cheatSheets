## Extract APK

<p><b>Step.1 : </b> Rename .apk file to .zip file. Extract it and you get the classes.dex file</p>
<p><b>Step.2 : </b> <a href="https://sourceforge.net/projects/dex2jar/">Download dex2jar</a> and set System Variables</p>
<p><b>Step.3 : </b> Open Terminal</p>

```
d2j-dex2jar classes.dex
```

<p><b>Step.4 : </b> <a href="http://java-decompiler.github.io/">Download jd-gui</a> and open .dex2jar file in jd-gui and save it as src name ( Only java file you get )</p>
<p><b>Step.5 : </b> <a href="https://ibotpeaches.github.io/Apktool/">Download apktool</a> and set System Varibles</p>
<p><b>Step.6 : </b> Open Terminal</p>

```
apktool d myapk.apk
```

<p><b>Step.7 : </b> Merge both folder and Enjoy the app Source</p>

<br><hr>
<p align="center"><b>OR</b></p>
<hr><br>
<p><b>Step.1 : </b> <a href="https://sourceforge.net/projects/dex2jar/">Download dex2jar</a> and set System Variables</p>
<p><b>Step.2 : </b> Open Terminal</p>

```
d2j-dex2jar -f myapk.apk
```

<p><b>Step.3 : </b> <a href="http://java-decompiler.github.io/">Download jd-gui</a> and open .jar file in jd-gui</p>
<p><b>Step.4 : </b> <a href="https://ibotpeaches.github.io/Apktool/">Download apktool</a> and set System Varibles</p>
<p><b>Step.5 : </b> Open Terminal</p>

```
apktool d myapk.apk
```

<p><b>Step.6 : </b> Do changes in Codes as you want</p>
<p><b>Step.7 : </b> Open Terminal for ReBuild the Folder</p>

```
apktool b folderName
```

<p><b>Step.8 : </b> Sign Application</p>

```
// Create a key
keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000

// Sign the apk
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore my_application.apk alias_name
```

