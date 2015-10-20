#Mybase v7更新记录
返回[myBase-Info首页](https://github.com/gzhaha/myBase-Info)  

官网相关链接如下(Official website)：
[http://www.wjjsoft.com/mybase_v7_changelog.html](http://www.wjjsoft.com/mybase_v7_changelog.html)

> **注意：
> 以下仅为个人翻译版，均为个人理解。如对本翻译版本有疑问，请以官网内容为准并自行查阅以上官网相关内容。**  
> **The below translation is based on my personal understanding, always refer to the official website in case of any confusion.**

## Version 7.0.0 Beta-21 (Under development)
1. Plugin: Custom search scope  
插件：增加【搜索 -> 搜索选定范围】  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_110754.png"  width="50%" height="50%" />

2. Plugin: Custom page margin  
插件：增加【段落 -> 定制页面边距】  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-21_084433.png"  width="70%" height="70%" />

3. Plugin: Open folder location of shortcuts  
插件：对附件快捷方式增加【打开源文件夹】功能  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_111252.png"  width="60%" height="60%" />

4. Improvement: Open attached documents externally with the original file names  
增强：当用外部程序打开附件时使用附件原来的文件名

5. Improvement: Options to customize default paragraph attributes  
增强：自定义默认段落属性  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_111541.png"  width="80%" height="80%" />

6. Added: the 'Add info items' menu item within the Lable/Calendar view  
增加：在【日历】和【标签】视图加入“添加条目”  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-21_083540.png"  width="70%" height="70%" />

7. Bugfix: The Ctrl+Open hotkey accidentally causes the database to lock as Readonly  
修正：Ctrl+Open热键导致把数据库变成只读的问题

## Version 7.0.0 Beta-20
1. Plugin: Syntax highlight for source code (C/C++, Javascript, Java, C#, PHP, SQL, Perl, VB, Delphi, Ruby, GO, R, Python, Bash, Objective C, Swift, etc.)  
插件：增加代码高亮，支持(C/C++, Javascript, Java, C#, PHP, SQL, Perl, VB, Delphi, Ruby, GO, R, Python, Bash, Objective C, Swift, 等)

2. Plugin: Insert quick text from a list of user-defined *.q.txt files  
插件：增加使用自定义的 *.q.txt文件插入快捷文字

3. Plugin: Set background color of selected cells in HTML table  
插件：增加设置表格单元格背景色

4. Plugin: Resize HTML table  
插件：增加重设html表格宽度

5. Plugin: Resize selected columns within HTML tables  
插件：增加重设html表格列宽度

6. Plugin: Edit data fields [key=value] within a fillable form  
插件：增加添加编辑 [key=value] 格式的数据

7. Plugin: Custom table style for sophisticated (IT) users to edit CSS properties for the current table with in a fillable form  
插件：增加自定义表格风格插件，用户可以通过添加css属性实现。支持的css属性可以参考[http://www.w3.org/TR/CSS21/propidx.html](http://www.w3.org/TR/CSS21/propidx.html)

8. Plugin: Add comments on the currently selected HTML content (paragraphs)  
插件：对所选html内容当前段落加入评注，使用本功能后当鼠标放在html文本上将会出现相关评注内容。  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-15_220530.png"  width="50%" height="50%" />

9. Plugin: Import MS-Outlook items  
插件：增加导入MS-Outlook内容

10. Plugin: Import Mindmap items  
插件：增加导入Mindmap内容

11. Plugin: Export spider diagram  
插件：增加导出蜘蛛图

12. Plugin: Export ePub digital book  
插件：增加导出ePub文档

13. Plugin: Export Mindmap document  
插件：增加导出Mindmap文档

14. Plugin: Export data records to CSV file  
插件：增加导出 [key=value] 格式的数据到csv文件  

15. Plugin: Export text with indentation  
插件：增加导出带缩进的纯文本文件

16. Plugin: Recovery database  
插件：增加恢复数据库插件，可以通过菜单【文件 -> 维护】找到  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-10_104413.png"  width="70%" height="70%" />

17. Enhancement: Enabled item HTML content to embed (link) local images stored in the database folder  
增强：信息节点可以嵌入（链接）保存于数据库中的图片

18. Enhancement: Enabled the plugin 'Edit plain text' to work with .md documents  
增强：编辑纯文本可以打开和编辑md附件

19. Enhancement: auto-load preferred markdown content (.md attachment) if any existing in an info item  
增强：自动加载信息节点中的md附件

20. Enhancement: auto-load preferred source code (.c/cpp/h/java/js/py/mm... attachments) if any existing in an info item, with source code syntax-highlighted  
增强：自动加载并渲染附件里的源码文件（.c/cpp/h/java/js/py...）

21. Enhancement: auto-load image gallery for info items that only contain image (jpg/png/gif/bmp) attachments  
增强：自动加载并显示附件图片
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-11_220857.png"  width="95%" height="95%" />

22. Enhancement: Attempts to download linked images via http when copying HTML content from web browsers  
增强：当从网页复制内容时，尝试下载链接图片

23. Enhancement: Refactor most of existing js plugins with the new JSAPI input() function for better usability  
增强：使用新的JSAPI input()重新编写大部分js插件

24. Enhancement: more HTML table editings (table/columns resizing, background color, and custom style)  
增强：更丰富的表格编辑功能

25. Enhancement: define bookmarks for paragraphs inside HTML content  
增强：在html内定义书签，节点内容内部书签（锚点）

26. Enhancement: more features with the Reminder window  
增强：提醒窗口提供更多功能

27. Enhancement: click column headers to sort plugin items  
增加：插件管理窗口可以对插件排序

28. Enhancement: check/uncheck individual text attributes on defining stylesheets  
增强：可以使用stylesheets自定义文本格式

29. Improvement: better performance with inserting plain text into HTML content  
改进：提升插入纯文本的性能

30. Improvement： better performance with listing labelled info items  
改进：提升列出标签条目性能

31. Improvement: clear extra spaces and returns in Html2Text parser  
改进：提升Html2Text分析程序去除多余空格功能

32. JSAPI: added a new paramater into plugin.setTextContent(), for loading HTML content or non-HTML content to be rendered and displayed in the HTML editor  
JSAPI：为[plugin.setTextContent()](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_setTextContent)加入一个新参数

33. JSAPI: added a new function plugin.setDomReadonly(), for toggling the readonly or editable flag within the HTML editor  
JSAPI：增加新函数[plugin.setDomReadonly()](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_setDomReadonly)

34. JSAPI: changes to the API function plugin.getSelectedAttachments(), for consistency with the new API Specs.  
JSAPI：修改[plugin.getSelectedAttachments()](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_getSelectedAttachments)

35. JSAPI: added a new function input(), for displaying multiple input fields in a popup window  
JSAPI：增加新函数[input()](http://www.wjjsoft.com/mybase_v7_jsapi.html#input)

36. JSAPI: added the CAppWord class and relevant member functions, for data exchange with MS-Word via OLE-Automation  
JSAPI：增加[CAppWord](http://www.wjjsoft.com/mybase_v7_jsapi.html#CAppWord)类

37. JSAPI: added the CAppOutlook class and relevant member functions, for data exchange with MS-Outlook via OLE-Automation  
JSAPI：增加[CAppOutlook](http://www.wjjsoft.com/mybase_v7_jsapi.html#CAppOutlook)类

38. JSAPI: added the CByteArray class, for maniplulating a series of bytes within an Array  
JSAPI：增加[CByteArray](http://www.wjjsoft.com/mybase_v7_jsapi.html#CByteArray)类

39. JSAPI: added the CZip class, for creating and accessing .zip archives  
JSAPI：增加[CZip](http://www.wjjsoft.com/mybase_v7_jsapi.html#CZip)类

40. JSAPI: added the CCanvas class, for painting and drawing with in-memory canvas  
JSAPI：增加[CCanvas](http://www.wjjsoft.com/mybase_v7_jsapi.html#CCanvas)类

41. JSAPI: added a new function platform.getClipboardText(), for retrieving text content from Clipboard  
JSAPI：增加[platform.getClipboardText()](http://www.wjjsoft.com/mybase_v7_jsapi.html#platform_getClipboardText)类

42. JSAPI: added a new function platform.setClipboardText(), for copying text content to Clipboard  
JSAPI：增加[platform.setClipboardText()](http://www.wjjsoft.com/mybase_v7_jsapi.html#platform_setClipboardText)类

43. Added the 'List unlabelled info items' utility  
增加：列出未加标签的条目

44. Added a few pre-defined stylesheet items  
增加：预设的一些stylesheet

45. Added a dialog box for inserting custom HTML table  
增加：为插入html表格功能添加对话框

46. Added the 'Open default content' and 'Auto-select to open' tool button on the content header bar  
增加：在条目内容标题栏上方加入“打开缺省文本内容”和“自动显示首选内容”按钮  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-14_125056.png"  width="50%" height="50%" />

47. Added 'Custom styles' for individual info items to be highlighted in different font name/size/styles/colors  
增加：自定义大纲文字的字体，颜色，大小等

48. Added the 'Delete' button in the 'Attachment - Open with' dialog box  
增加：在【附件 -> 打开方式 -> 指定程序打开】对话框增加删除按钮  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-11_223737.png"  width="70%" height="70%" />

49. Added the 'Show lines' option for the Outline tree view  
增加：在【查看 -> 选项 -> 大纲】加入“显示大纲连线”的选项  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-12_104648.png"  width="60%" height="60%" />  

50. Added the 'Find/Replace' function in the 'Edit plain text' and 'Edit Html source' plugins  
增加：在“编辑HTML源代码”和“编辑纯文本”加入“寻找/替换”功能  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-12_104800.png"  width="70%" height="70%" />

51. Added the 'Font size' option in the 'Edit plain text' and 'Edit Html source' plugins  
增加：在“编辑HTML源代码”和“编辑纯文本”加入定义字体大小的选项

52. Added the 'Bookmark' button in the 'Edit hyperlink' dialog box  
增加：“编辑链接”窗口增加链接到书签的功能  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-12_104859.png"  width="70%" height="70%" />

53. Added the 'Line spacing' option for default HTML formatting  
增加：默认html格式增加定义行距的选项  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-14_124947.png"  width="60%" height="60%" />

54. Added the 'Including trashed entries' option for replicating .nyf database  
增加：复制数据库增加“包括删除条目”的选项  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-08-12_104935.png"  width="50%" height="50%" />

55. Added the 'Markdown document.md' option in the [Attachments - New attachment] menu  
增加：【附件 -> 新建附件】加入Markdown document.md

56. Added the 'search all opened database' option in the Advanced Search form  
增加：在高级搜索里加入“搜索所有当前已打开数据库”的选项

57. Added the backup policy, custom backup path and relevant options  
增加：加入备份数据库相关选项。【查看 -> 选项 -> 备份】

58. Bugfix: the outline pane may not show up if the pane was kept hidden at last exit  
修正：大纲在上次关闭程序时为隐藏状态时，再次打开程序不显示的问题

59. Bugfix: the 'Replace text' utility not working in the HTML editor  
修正：html编辑器中替换文本不能正常工作的问题

60. Minor changes  
其他小更改


## Version 7.0.0 Beta-19 ##
1. Tool button: 'Insert hyperlink ...'  
添加工具栏按钮“插入网址”

1. Tool button: 'Insert attachment link ...', with multi-selection enabled  
添加工具栏“插入附件链接”，支持多选批量插入

1. Allow to copy/paste cells/rows/tables from MS-Excel  
支持从MS-Excel复制表格，行。

1. Auto-import linked images (if any) when copying HTML contents from MS-Word  
复制MS-Word里html内容时自动导入带链接的图片

1. Fix: ignore duplicate image links when copying online HTML contents  
修正：复制html时忽略相同图片链接的问题。

1. Bugfix: backslashes not working when copying HTML content  
修正：复制html时，反斜杠（\）不生效的问题。

1. Bugfix: hyperlinks to local files (e.g. file:///d:/dir/...) may not work  
修正：到本地文件链接 (e.g. file:///d:/dir/...)不生效的问题。

1. Bugfix: custom icons' label text not replicated while replicating database  
修正：复制数据库时自定义图标名称丢失的问题。

1. JSAPI bindings for MS-Word (Windows)  
MS-Word与JSAPI的绑定（Windows版）

1. Export MS-Word outline (Windows)  
导出MS-Word大纲（Windows版）

1. Import MS-Word outline (Windows)  
导入MS-Word大纲（Windows版）

1. Bugfix: a bug in the HTML document parser with self-closing HTML elements may cause the program to crash during indexing/searching  
修正：索引，搜索时崩溃的问题

1. Bugfix: custom text styles (bold/italic/underline) not working for new item content  
修正：自定义文字格式（加粗，斜体，下划线）在新条目内容不生效的问题

1. Show item titles on the status-bar during indexing  
搜索时状态条线索当前条目的标题

1. Workaround: within the inbuilt HTML editor, Text Input Method not working well on dark backgrounds (HSV:V<128)  
在HTML编辑器里，由于背景为深色不显示输入内容的问题

1. Added the Capture/Share menus; The Capture menu contains 'Import ...' specific utilities, while the Share menu contains 'Export ...' specific utilities  
加入 捕获 和 分享 菜单

1. Plugin: Tools - Reveal internal data, which allows to view and modify internal data files; Do not modify internal data files by hand unless you have to fix broken links  
增加 工具 - 内部链接数据 工具

1. Enabled clipboard monitor to download linked images when copying web contents from web browsers or MS-Word  
剪贴板监视加入图片下载支持

1. Enabled clipboard monitor to copy contents from MS-Word/Excel including tables/cells/images  
剪贴板监视加入从 MS-Word/Excel复制表格图片的支持

1. Added the Paragraph menu, which contains the paragraph specific formatting utilities  
加入段落菜单（包含段落相关设置的工具）

1. Added: Paragraph - Single line spacing, One and half line spacing and Double line spacing  
加入 段落 - 单倍行距，1.5倍行距，2倍行距

1. Bugfix: line-spacing not working well with multiple paragraphs selected  
修正：行间距在多段选择时的问题


## Version 7.0.0 Beta-18 ##
1. WebCollect addon for Mozilla Firefox  
用于Firefox浏览器的WebCollect插件

1. WebCollect addon for Google Chrome  
用于Google Chrome浏览器的WebCollect插件

1. Context menu: Copy image  
复制图片

1. Context menu: Copy image URL  
实用工具（图片）：复制图片链接

1. Context menu: Save image as  
实用工具（图片）：图片另存为

1. Context menu: Resize image  
实用工具（图片）：图片尺寸

1. Context menu: Rotate image  
实用工具（图片）：旋转图片

1. Auto-download linked images (if any) when copying HTML content from web browsers  
从浏览器复制html内容时，自动下载链接图片

1. Auto-grab linked images (if any) when copying HTML content from MSWord  
从word复制html内容时自动获取链接图片

1. Drag-drop embedded images into the attachment list to save the image data as attachments  
把html里嵌入的图片拖到附件栏，会以附件形式保存图片

1. Drag-drop attached png/jpg/gif/bmp files into HTML editor to insert the images into HTML content  
拖图片附件png/jpg/gif/bmp进html编辑器，即可插入图片

1. Drag-drop non-graphic attachments into HTML editor to insert hyperlinks  
拖非图片附件进html编辑器，即可插入链接

1. Drag-drop info items into HTML editor to make hyperlinks; The CTRL key modifier is needed to be held down while dragging info items into current item content  
按ctrl按钮的同时，把条目拖到html编辑器即插入链接。

1. Support of hyperlinks to attachments stored in either current or any other info items; Clicking on a hyperlink triggers the linked attachment to be open externally with the associated program  
在编辑链接框中，通过“插入附件链接”菜单，支持链接到任意节点的附件链接。

1. Edit - Text Utilities: Make selected text fields into HTML table  
编辑 - 实用工具（文本）：转换文本为表格

1. Edit - Text Utilities: Make selected text upper/lower case  
编辑 - 实用工具（文本）：转换为大写，小写字母

1. Edit - Text Utilities: Sort selected text lines  
编辑 - 实用工具（文本）：文本行排序

1. Edit - Text Utilities: Remove unwanted spaces from selected text  
编辑 - 实用工具（文本）：清除多余空白

1. Customizable zoom level for tool buttons, so it can work with high resolution monitors  
增加“工具按钮显示缩放系数”，可以调高系数便与在高分辨率屏幕上使用

1. Display a lighter text in database Tabs with unified title bar on Mac  
改进Mac系统上文字显示

1. Substituted inbuilt file parser for external txt/htm DLLs to parse text/html content during indexing and searching  
使在索引和搜索时使用用自带dll分析。

1. Added the monthly calendar view  
添加日历月视图

1. Drag-drop .nyf file into main window to be open as database  
当把.nyf文件拖到主窗口将会打开此数据库文件

1. Syntax highlighter for html source  
编辑html源代码语法高亮

1. Save and restore toolbar position  
保存，恢复工具栏位置