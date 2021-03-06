# FMXComponents

Main site: https://github.com/zhaoyipeng/FMXComponents <br>
Mirror site: https://gitee.com/zhaoyipeng/FMXComponents <br>

This project includes the components that donors and I have actually used in applications.<br> 
If you have some components want to add into this project, you can send it to zhaoyipeng@hotmail.com

本项目包括本人及捐赠人实际应用中使用的控件

技术支持QQ群: 513799640<br>
Support QQ Group: 513799640<br>
![FMXComponents](SnapShots/group_qrcode.jpg)  <br>
You can also add my skype: zhaoyipeng@hotmail.com<br>

## 17. PhotoCorrect<br>
![FMXGR32Demo2](SnapShots/FMXGR32Demo2.gif)  
I have not much time, so this release just source code, not component yet.<br>
最近时间不多，没有封装成控件，先发布了实现源码。<br>

## 16.TFMXRotatingText<br>
A Firemonkey Rotating Text Component be inspired by RotatingText(https://github.com/sdsmdg/RotatingText)<br>
![FMXRotatingText](SnapShots/FMXRotatingText.gif)  <br>

## 15.INativeCanvas

We know the firemonkey's canvas is very bad quality on mobile platforms<br>
![FiremonkeyCanvas](SnapShots/FiremonkeyCanvas.png)  <br>

After Aone's hard work we can use native method drawing the graph, you can get same quality as native mobile platform, Aone's method is using helper class to TCanvas, you must static decide use native or firemonkey to draw graph, I changed it to a INativeCanvas interface, you can change the method at runtime.

![INativeCanvas](SnapShots/INativeCanvas.png)  <br>

this is the compare of Firemonkey Canvas and INativeCanvas FillText method<br>

![iOSFMXCanvas](SnapShots/iOSFMXCanvas.png)  <br>
![iOSNativeCanvas](SnapShots/iOSNativeCanvas.png)  <br>


All you need is add several lines.

```pascal
procedure TFMXCallout.Paint;
var
  Canvas: INativeCanvas;
  Method: TDrawMethod;
begin
  if Self.NativeDraw then
    Method := TDrawMethod.Native
  else
    Method := TDrawMethod.Firemonkey;
  Canvas := Self.Canvas.ToNativeCanvas(Method);

  Canvas.NativeDraw(LocalRect, procedure begin // 原生繪圖 by Aone, 暱名函數裡加入繪圖方法, 內部會先畫到 Bitmap
    Canvas.FillPath(FFillPath, AbsoluteOpacity, Fill);
    Canvas.DrawPath(FPath, AbsoluteOpacity, Stroke);
  end);                                       // 原生繪圖 by Aone, 結束後會顯示這個 Bitmap
end;
```

## 14.TFMXCallout

This component wrote by Aone, it's also a very good demo of the INativeCanvas. Thanks a lot to Aone.

![TFMXCallout](SnapShots/FMXCallout.gif)  <br>

## 13.graphics32 for Firemonkey

![FMXGR32Demo](SnapShots/FMXGR32Demo.gif)  

Firemonkey version of Graphics32 [graphics32-for-Firemonkey](https://github.com/zhaoyipeng/graphics32-for-Firemonkey)

You must download the graphics32-for-Firemonkey source code to compile demo project.


## 12.TFMXLoadingIndicator  <font color=red size=12>(New)</font>

![TFMXLoadingIndicator](SnapShots/FMXLoadingIndicator.gif)  

Loading indicator port from [LoadingIndicators.WPF](https://github.com/100GPing100/LoadingIndicators.WPF)
 
## 1.TFMXScrollableList

![TFMXScrollYears](SnapShots/FMXScrollableList.gif)  

A Simple Firemonkey Scrolleable List Component  

这是一个简单的滚动列表控件，可以用于选择年份或其它信息  
 
选项使用 Items 属性  


## 2.TFMXRatingBar  

![TFMXRatingBar](SnapShots/FMXRatingBar.gif)<br>

![TFMXRatingBarComponentEditor](SnapShots/FMXRatingBarED.gif)<br>

A Simple Rating BarComponent  

这是一个简单的评级控件，目前只支持显示 
 
Rating property is Value  

评级属性为Value  

## 3.TFMXCircleScoreIndicator

![TFMXCircleScoreIndicator](SnapShots/FMXCircleScoreIndicator.gif)  

A Simple Circle Score Indicator  

这是一个简单的成绩显示控件  
 

score property is Value  

成绩属性为Value  

## 4.TFMXImageSlider

![TFMXImageSlider](SnapShots/FMXImageSlider.gif)  

A Simple Image Slider

一个简单的图片轮播控件（还不完善）
 
## 5.TFMXSimpleBBCodeText

![TFMXSimpleBBCodeText](SnapShots/FMXSimpleBBCodeText.gif)  

A Simple BBCode Text Display Control 

一个简单的BBCode显示控件，实现简单的富文本显示

感谢 龟山Aone 的提示，TFMXSimpleBBCodeText性能得到了极大地优化，基本达到实用程度

## 6.[TFMXGuesturePassword](Documents/FMXGesturePassword.md)

![TFMXGuesturePassword](SnapShots/FMXGuesturePassword.gif)  

A Guesture Password input Control 

手势密码输入控件

## 7.[TFMXCalendarControl](Documents/FMXCalendarControl.md)

![TFMXCalendarControl](SnapShots/FMXCalendarControl.gif)  

A calendar component like iOS style

类似iOS风格的日期控件

## 8.[百度地图SDK](BaiduMapSDK/)

### 感谢 xubzhlin 的捐献<br>
BaiduMap SDK for Firemonkey<br>
百度地图SDK

## 9.TFMXSeg7Shape

Segment 7 Shape Firemonkey Componet create by Yamasho

![Seg7ShapeFmx](SnapShots/FMXSeg7Shape.gif)  

七段式数字显示控件

原始项目地址为：
https://github.com/qa65000/Seg7ShapeFmx

## 10.TFMXToast

![TFMXToast](SnapShots/FMXToast.gif)  

TFMXToast is a toast component using pure fmx<br>
使用纯FMX的Toast控件<br>
参考了Aone的文章：http://www.cnblogs.com/onechen/p/7130227.html <br> 

## 11.TFMXQRCode

![TFMXQRCode](SnapShots/FMXQRCode.gif)  

A QRCode display component<br>
use DelphiZXingQRCode to generate QRCode image<br>

## License

The FMXComponents is open-sourced software licensed under the [MIT License](LICENSE).

