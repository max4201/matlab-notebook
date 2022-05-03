# MATLAB混和編程
## MATLAB compiler

Q:什麼是MATLAB編譯器(Matlab compiler)?

A:...

Q:誰需要他?

https://www.youtube.com/watch?v=DWzpBEGrMs4
http://www.icodeguru.com/9/1049.html
http://blog.csdn.net/u011475134/article/details/72852085
https://cn.mathworks.com/matlabcentral/answers/182851-how-do-i-integrate-my-c-shared-library-generated-from-matlab-r2013b-in-visual-studio-2013

+ 安裝軟體

前言:
後來的MATLAB都不附加編譯器了，需要使用者自己去裝別人家的，有很多家最主流的就是微軟的，我只找最簡單裝然後可以用的。

可以用的環境:
1.  這個還沒測試完
Windows 10 64bit 
Matlab R2009a 64bit (約3GB硬碟空間) 
搭配擇一:

1.1. VS2008(約??GB，還沒測試)。

**提示:** 其實需要的是微軟的C/C++編譯器。
**提示:** R2009a的年代還沒有Matlab Coder。

2. Windows 10 64bit 
Matlab R2013a 64bit (約3GB硬碟空間) 
搭配擇一:

2.1. VS2010(約6GB硬碟空間)，已經測試OK，但細節要找時間寫清楚並測試。

**提示:** 其實需要的是微軟的C/C++編譯器。

+ 編譯器設定心得

在Matlab命令列中輸入mex -setup與mbuild -setup，按照指示操作，細節我就不提。
要註明的是，如果你發現自動找的清單裡面沒有，試試看以下的做法:
所有問題都回答[n]，然後編譯器選[0]:None。做完之後再重新執行mex -setup與mbuild -setup設定一次，有時候就會跑出清單了。
