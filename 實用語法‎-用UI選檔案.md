# MATLAB實用語法
## MATLAB用UI選檔案
**使用平台:**

*Windows 10 64bit*

**MATLAB版本:**

*MATLAB R2013a 64bit*

**說明:**

*用視窗介面選擇檔案。*

**Matlab Script:**
```matlab
%==========================================================================
% 取得檔名的UI
%
[filename, pathname] =...
    uigetfile(...
                {...  
                    '*.csv','csv (*.csv)';...%第1個篩選項目
                    '*.*','All Files (*.*)'...%第2個篩選項目
                },...
                'Pick a file',...%UI標題
                'MultiSelect', 'off'...%是否允許多選
            );
%==========================================================================
%==========================================================================
% 檔名轉為細胞矩陣
%--
if (iscell(filename) == 0)
    inputname{1}=filename;
elseif (iscell(filename) == 1)
    inputname=filename;    
end
%--
% 展示第一個檔名
%disp([pathname,inputname{1}])
%==========================================================================
```
