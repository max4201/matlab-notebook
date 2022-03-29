# MATLAB實用語法
## MATLAB的uitable技巧
```matlab
clear;clc;close all
%==========================================================================
% 岩石電阻率分佈資訊，標頭部分。
%--
Rock_Resistivity_Info={'岩石種類','岩石代表','電阻率範圍下界[Ohm-m]','電阻率範圍上界[Ohm-m]'};
Rock_Resistivity_Info_index=1;
%==========================================================================
%==========================================================================
% 岩石電阻率分布資訊，#1
% 岩石種類: 顯著的導電礦物
% 岩石代表: 石墨，塊狀硫化物。
%--------------------------------------------------------------------------
% 石墨，電阻率範圍: 0.1~10 [ohm-m]
Rock_Type_str='顯著的導電礦物';
Rock_Example_str='石墨';
Rock_Resistivity_min_str='0.1';
Rock_Resistivity_max_str='10';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 塊狀硫化物，電阻率範圍: 0.01~1 [ohm-m]
Rock_Type_str='顯著的導電礦物';
Rock_Example_str='塊狀硫化物';
Rock_Resistivity_min_str='0.01';
Rock_Resistivity_max_str='1';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 岩石電阻率分布資訊，#2
% 岩石種類: 水、流體
% 岩石代表: 海冰，海水，淡水，凍土。
%--------------------------------------------------------------------------
% 海冰，電阻率範圍: 400~100000 [ohm-m]
Rock_Type_str='水、流體';
Rock_Example_str='海冰';
Rock_Resistivity_min_str='400';
Rock_Resistivity_max_str='100000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 海水，電阻率範圍: 0.2~1 [ohm-m]
Rock_Type_str='水、流體';
Rock_Example_str='海水';
Rock_Resistivity_min_str='0.2';
Rock_Resistivity_max_str='1';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 淡水，電阻率範圍: 2.5~100 [ohm-m]
Rock_Type_str='水、流體';
Rock_Example_str='淡水';
Rock_Resistivity_min_str='2.5';
Rock_Resistivity_max_str='100';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 凍土，電阻率範圍: 400~100000 [ohm-m]
Rock_Type_str='水、流體';
Rock_Example_str='凍土';
Rock_Resistivity_min_str='400';
Rock_Resistivity_max_str='100000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 岩石電阻率分布圖#3
% 岩石種類: 風化的地層岩石
% 岩石代表: 變質岩，火成岩:鐵鎂質的~長英質的，鐵質岩殼。
%--------------------------------------------------------------------------
% 變質岩，電阻率範圍: 10~2000 [ohm-m]
Rock_Type_str='風化的地層岩石';
Rock_Example_str='變質岩';
Rock_Resistivity_min_str='10';
Rock_Resistivity_max_str='2000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 火成岩:鐵鎂質~長英質，電阻率範圍: 2~200 [ohm-m]
Rock_Type_str='風化的地層岩石';
Rock_Example_str='火成岩:鐵鎂質~長英質';
Rock_Resistivity_min_str='2';
Rock_Resistivity_max_str='200';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 鐵質岩殼，電阻率範圍: 2000~30000 [ohm-m]
Rock_Type_str='風化的地層岩石';
Rock_Example_str='鐵質岩殼';
Rock_Resistivity_min_str='2000';
Rock_Resistivity_max_str='30000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 岩石電阻率分布圖#4
% 岩石種類: 沉積物
% 岩石代表: 冰磧土，黏土，礫石和砂。
%--------------------------------------------------------------------------
% 冰磧土，電阻率範圍: 50~2000 [ohm-m]
Rock_Type_str='沉積物';
Rock_Example_str='冰磧土';
Rock_Resistivity_min_str='50';
Rock_Resistivity_max_str='2000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 黏土，電阻率範圍: 4~100 [ohm-m]
Rock_Type_str='沉積物';
Rock_Example_str='黏土';
Rock_Resistivity_min_str='4';
Rock_Resistivity_max_str='100';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 礫石和砂，電阻率範圍: 400~10000 [ohm-m]
Rock_Type_str='沉積物';
Rock_Example_str='礫石和砂';
Rock_Resistivity_min_str='400';
Rock_Resistivity_max_str='10000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 岩石電阻率分布圖#5
% 岩石種類: 沉積岩
% 岩石代表: 褐煤~煤，白雲岩~石灰岩，頁岩，砂岩~礫岩。
%--------------------------------------------------------------------------
% 褐煤~煤，電阻率範圍: 10~400 [ohm-m]
Rock_Type_str='沉積岩';
Rock_Example_str='褐煤~煤';
Rock_Resistivity_min_str='10';
Rock_Resistivity_max_str='400';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 白雲岩~石灰岩，電阻率範圍: 1000~10000 [ohm-m]
Rock_Type_str='沉積岩';
Rock_Example_str='白雲岩~石灰岩';
Rock_Resistivity_min_str='1000';
Rock_Resistivity_max_str='10000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 頁岩，電阻率範圍: 5~30 [ohm-m]
Rock_Type_str='沉積岩';
Rock_Example_str='頁岩';
Rock_Resistivity_min_str='5';
Rock_Resistivity_max_str='30';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%--------------------------------------------------------------------------
% 砂岩~礫岩，電阻率範圍: 50~10000 [ohm-m]
Rock_Type_str='沉積岩';
Rock_Example_str='砂岩~礫岩';
Rock_Resistivity_min_str='50';
Rock_Resistivity_max_str='10000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 岩石電阻率分布圖#6
% 岩石種類:未風化的火成岩和變質岩
% 岩石代表: 火成岩和變質岩
%--------------------------------------------------------------------------
% 火成岩和變質岩，電阻率範圍: 1000~100000 [ohm-m]
Rock_Type_str='未風化的火成岩和變質岩';
Rock_Example_str='火成岩和變質岩';
Rock_Resistivity_min_str='1000';
Rock_Resistivity_max_str='100000';
%--
% 整理
Rock_Resistivity_Info_index=Rock_Resistivity_Info_index+1;
Rock_Resistivity_Info(Rock_Resistivity_Info_index,:)={Rock_Type_str,Rock_Example_str,Rock_Resistivity_min_str,Rock_Resistivity_max_str};
%==========================================================================
%==========================================================================
% 產生uitable表格，來展示內容
%--------------------------------------------------------------------------
% 建立UI用的figure並設定為不可視，尺寸設定640x660
ui_figure_handle = figure('OuterPosition',[1,1,640,581],'Visible','off');
%--
% 設定其他figure參數
%--
% 不可改變figure大小。
set(ui_figure_handle,'Resize','off')
% 隱藏選單列
set(ui_figure_handle,'MenuBar','none')
% 隱藏工具列
set(ui_figure_handle,'ToolBar','none')
% 隱藏figure數字
set(ui_figure_handle,'NumberTitle','off')
% 設定figure名稱
set(ui_figure_handle,'Name','岩石電阻率分佈資訊(粗略估計，參考Palacky,1987)')
% 移動到螢幕中間
movegui(ui_figure_handle,'center')
% 改為可視
set(gcf,'Visible','on');
%--
% 取得figure內部位置資訊
figure_inner_position=get(ui_figure_handle,'Position');
% 調整幾乎填滿figure(可能不太準確要微調)
uitable_handle = uitable(ui_figure_handle,'Position',[0,0,figure_inner_position(3)+11, figure_inner_position(4)+11]);
%--
% 設定uitable寬度
uitable_column_width = 149;
set(uitable_handle,'ColumnWidth',{uitable_column_width,uitable_column_width,uitable_column_width,uitable_column_width});
% 設定uitable標頭
uitable_header_strings=Rock_Resistivity_Info(1,:);
uitable_html_header_strings = strcat('<html><tr align="center" ><td width=',num2str(uitable_column_width),'><font size=5>',uitable_header_strings);%後半部分HTML可省略
set(uitable_handle,'ColumnName', uitable_html_header_strings);%uitable支援HTML格式的資料，換句話說填入資料受限HTML格式，有必要的話要使用跳脫字元。
%--
% 設定uitable資料格式
set(uitable_handle,'ColumnFormat', {'char','char','char','char'});
% 整理成HTML格式
uitable_data_strings = strcat('<html><tr align="center" ><td width=',num2str(uitable_column_width),'><font size=3>',  Rock_Resistivity_Info(2:end,:));
set(uitable_handle,'Data',uitable_data_strings);
%uitable_data_strings(1)
set(uitable_handle,'FontSize',14);
% 設定uitable不可選表格
set(uitable_handle,'Enable','inactive')
%==========================================================================
```
