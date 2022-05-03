# 實用語法
## MATLAB讀CSV有檔頭
[A,B,C]=textread(csv_file_name,'%s%s%s','delimiter',',','headerlines',0)
+ **方法:**
**使用平台:**

*Windows 10 64bit*

**MATLAB版本:**

*MATLAB R2013a 64bit*

**說明:**

*將所有逗號分隔的CSV檔案以文字方式全部讀入，解析出標頭與資料，自動判斷數量。*


**Matlab Script:**
```matlab
clear;clc;close all
%==========================================================================
% 內建MATLAB函數 textread 使用心得
% 有多種模式，介紹最常用的模式，即:
% [...]=textread('filename',format,read_line_count,'delimiter',','headerlines',skip_header_line_count) 
% format，與C語言scanf類似的格式，允許多個，例如:'%s%s'，但是中間不需要分隔符號，format中的數量與輸出變數數量相同。
% read_line_count為整數，若大於等於0則為指定數量，小於0就是讀到檔尾。
% skip_header_line_count為整數，處理時會跳過的行數(檔頭部份)。
% 注意: textread應該依賴MATLAB設定編碼，通常是ansi，UTF-8之類的可能要動手腳處理一下。
%--
% CSV檔名
CSV.filename='rain_station_ansi.csv';
%--
% 讀取標頭行
temp_header_line=textread(CSV.filename,'%s',1,'delimiter','\n','headerlines',0);
% 使用正則表達式將標頭以逗號「,」拆解為多個，存在多層細胞陣列中
temp_split_str_cell = regexp(temp_header_line, ',', 'split');
% 取出拆解後的CSV標頭
CSV.DataHeader=temp_split_str_cell{1};
% 計算標頭數量(有幾個直行)
temp_vertical_column_count=length(CSV.DataHeader);
%==========================================================================
%==========================================================================
% 按照直行數量來讀取CSV資料，且全部資料都視為文字來處理。
% 視為文字應該會寫成 '%s%s%s%s%s%s%s%s%s'
% 可用remat處理:
% repmat('%s',1,temp_vertical_column_count)
%--
[temp_data{1:temp_vertical_column_count}]=textread(CSV.filename,repmat('%s',1,temp_vertical_column_count),-1,'delimiter',',','headerlines',1);
CSV.Data=[temp_data{1:temp_vertical_column_count}];
%==========================================================================
```
