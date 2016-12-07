# ZbarScanLib
##一个简单的可以扫码和生成二维码的库 <br>
###基本介绍<br>
常见的二维码扫描库多是基于Zxing的，功能强大，但是在扫描复杂二维码时速度较慢，Zbar是基于C编写的库，扫描的速度快。但是Zbar库的内容比较少，所以我修改了默认的CaptureActivity类，添加了声音和震动效果，并基于Zxing:Code添加生成二维码的功能。为了方便夜间使用，还添加了手电筒。具体使用方法参见demo。<br>
###所需权限<br>
因为为扫描成功提示添加了震动效果，所以除了相机权限外还需要添加震动权限。<br>
 uses-permission android:name="android.permission.CAMERA"<br>
 uses-permission android:name="android.permission.VIBRATE"<br>
###添加依赖<br>
1、在project.gradle里添加maven<br>
allprojects {<br>
		repositories {<br>
			...<br>
			maven { url 'https://jitpack.io' }<br>
		}<br>
	}<br>
2、在Module.gradle里添加compile<br>
compile 'com.github.JN-caiwei:ZbarScanLib:v1.0'<br>

