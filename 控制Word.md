# MATLAB控制Word

```matlab
clear;clc
%
%REF:https://www.mathworks.com/examples/matlab/community/32866-word-commands-with-actxserver
%REF2:https://docs.microsoft.com/en-us/previous-versions/office/developer/office-2007/bb238158(v=office.12)
% Version Information
% Version Added:
% Name Value Description
% wdFormatDocument 0 Microsoft Office Word format.
% wdFormatDOSText 4 Microsoft DOS text format.
% wdFormatDOSTextLineBreaks 5 Microsoft DOS text with line breaks preserved.
% wdFormatEncodedText 7 Encoded text format.
% wdFormatFilteredHTML 10 Filtered HTML format.
% wdFormatHTML 8 Standard HTML format.
% wdFormatRTF 6 Rich text format (RTF).
% wdFormatTemplate 1 Word template format.
% wdFormatText 2 Microsoft Windows text format.
% wdFormatTextLineBreaks 3 Windows text format with line breaks preserved.
% wdFormatUnicodeText 7 Unicode text format.
% wdFormatWebArchive 9 Web archive format.
% wdFormatXML 11 Extensible Markup Language (XML) format.
% wdFormatDocument97 0 Microsoft Word 97 document format.
% wdFormatDocumentDefault 16 Word default document file format. For Microsoft Office Word 2007, this is the DOCX format.
% wdFormatPDF 17 PDF format.
% wdFormatTemplate97 1 Word 97 template format.
% wdFormatXMLDocument 12 XML document format.
% wdFormatXMLDocumentMacroEnabled 13 XML document format with macros enabled.
% wdFormatXMLTemplate 14 XML template format.
% wdFormatXMLTemplateMacroEnabled 15 XML template format with macros enabled.
% wdFormatXPS 18 XPS format.
%REF3:
%--------------------------------------------------------------------------
%開啟MS Word 主程式
MS_Word_App = actxserver('Word.Application');
%--
%設定可視
MS_Word_App.Visible =1;    
%--------------------------------------------------------------------------
%--------------------------------------------------------------------------
%新增文件
My_Documents=MS_Word_App.Documents.Add;
%--------------------------------------------------------------------------
%--------------------------------------------------------------------------
%設定游標
My_Selection=MS_Word_App.Selection;
%--------------------------------------------------------------------------
%--------------------------------------------------------------------------
%寫字
My_Selection.TypeText('Hello World!');
%換行
My_Selection.TypeParagraph;
%--------------------------------------------------------------------------
%--------------------------------------------------------------------------
%插入圖片
My_Selection.InlineShapes.AddPicture([pwd,'/test.png'],0,1);
My_Selection.InlineShapes.AddPicture([pwd,'/test.png'],0,1);
%--------------------------------------------------------------------------
%--------------------------------------------------------------------------
%另存新檔為
My_Documents.SaveAs2([pwd,'/test.doc'],0);         %save Document
My_Documents.SaveAs2([pwd,'/test.docx'],16);
My_Documents.SaveAs2([pwd,'/test.pdf'],17);         %save Document
MS_Word_App.Quit();
%--------------------------------------------------------------------------
```
