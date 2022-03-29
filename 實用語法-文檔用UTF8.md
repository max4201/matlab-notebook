# MATLAB實用語法
## MATLAB文檔用UTF8
用feature('DefaultCharacterSet')可以查詢目前用的文字編碼

用feature('locale')也可以查詢部分相關資訊

在許多時候會面臨讀/寫有碰到非英文語系的問題，強制使用UTF8是一個常見的選擇。
例如網頁幾乎都使用UTF8編碼，進行操作時盡量不改變編碼為主。

+ 寫檔:
f1=fopen(output_HTML_name,'w','n','UTF-8');
fclose(f1);

+ 讀檔:
f1=fopen(output_HTML_name,'r','n','UTF-8');
fclose(f1);

w=寫入(覆蓋舊檔)，r=讀取。
n=用系統原生機碼(也就是自動決定Big-endian等等的編碼)。
'UTF-8'= 使用UTF8編碼。
