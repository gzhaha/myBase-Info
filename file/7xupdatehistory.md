#myBase v7 更新记录
返回[myBase-Info首页](https://github.com/gzhaha/myBase-Info)  

官网相关链接如下(Official website)：
[http://www.wjjsoft.com/mybase_v7_changelog.html](http://www.wjjsoft.com/mybase_v7_changelog.html)

> **注意：
> 以下仅为个人翻译版，均为个人理解。如对本翻译版本有疑问，请以官网内容为准并自行查阅以上官网相关内容。**  
> **The below translation is based on my personal understanding, always refer to the official website in case of any confusion.**

## Version 7.0.0 Beta-23（正在开发中）

1. Added: the 'Relative path variables' feature  
   增加：相对路径变量功能

2. Plugin: File - Maintenance - Define relative path variable, which allows to add, modify and remove a relative path variable; Variable names accept A-Z, 0-9 and underscore, while values are the target directory paths without trailing slashes; Defining a variable with the value filed left blank to remove it.  
   插件：增加【文件 - 维护 - Define relative path variable】

3. Plugin: File - Maintenance - Apply relative path variables, which searches the current database for hyperlinks and shortcuts and attempts to apply relative path variables if applicable; This could be useful if you have previously inserted a lot of hyperlinks and/or shortcuts before this release.  
   插件：增加【文件 - 维护 - Apply relative path variables】

4. Added: the option to determine if the default HTML content should go into edit mode when opening the info item, and another option to determine if attached HTML documents should go into edit mode when opening the documents inplace;  
   增加：在【选项 - 内容】里添加【打开缺省HTML内容时自动进入编辑状态】和【打开HTML附件文档时自动进入编辑状态】选项

5. added: the context menu on database tabs with commands: New database, Open database, Close database, Close all databases, Close other databases  
   增加：在数据库标签添加【创建数据库】，【打开数据库】，【关闭】，【关闭全部】和【关闭其他】

6. added: an option to customize color for database tabs; Right-click on the database Tabs and select 'Tab color' menu item  
   增加：在数据库标签添加【库标签颜色】

7. added: an option to keep and restore the font size for the text box window used for displaying text from with in plugins  
   增加：被插件调用的文本框中字体大小将被保留。

8. Improvement: syntax-highlight: added MathLib keywords, constants and function calls; MathLib .m source files will also be rendered by syntax-highlighting when opening inplace, with a solution to resolve conflicts of .m suffix between objective-c and mathlib by detection of characteristic tags and syntax  
   增强：【源程序语法加亮】加入MathLib支持

9. Improvement: ability to change the database tab position by dragging-and-dropping the tabs  
   增强：数据库标签可进行拖拉移动

10. Improvement: ability to jump to the position/paragraph inside the document last visited when jumping back and forth between info items; Surely you can also define a bookmark to permanently save the position in the database  
    增强：跳转到另外的条目后可以返回之前的条目位置

11. Improvement: keep focus in search results pane so you can select items by using the keyboard, and press Enter/Space to trigger the currenly selected item  
    增强：焦点在搜索结果窗口，便于使用键盘上下选择和打开条目。

12. Improvement: Capture - Import directory tree: for HTML documents, it also tries to import linked images from the accompanying sub folder (e.g. ./xxx_files), and skip the accompanying sub folder when recursively running into sub directories;In addition, a bugfix to the javascript date/time garbage characters, and improvements with hyperlinks imported and formatted as HTML table  
    增强：【导入 - 导入磁盘目录树】，对于HTML文档，会尝试在相应子目录导入链接中的图片。另外对于链接和表格的导入也做了改进。

13. Improvement: Share - Export directory tree: it also handles shortcuts and file:// hyperlinks, and original documents linked with HTML contents if present will be copied into the target directory  
    增强：【导出 - 导出磁盘目录树】增加对快捷方式和file://超链接的处理。

14. Improvement: press Enter/Space to trigger items from the saved searches list  
    增强：【搜索 - 已存搜索项】中按回车/空格即进行搜索

15. Improvement: Share - Export CHM project: automatically decode embedded image data (BASE64) and save as image files, so the images can be viewed normally in CHM digital books without having to upgrade to the latest version of IE web browser  
    增强：【导出 - 导出CHM项目文件】将自动把以BASE64格式嵌入HTML的图片解码

16. Improvement: Organize - Display statistics: it also gives the current item's location text and ssg-path info  
    增强：【整理 - 显示条目统计】中会包含当前条目的位置信息和ssg路径信息

17. Improvement: with in the outline view, press Ctlr+C to copy the selected item titles  
    增强：在大纲中Ctlr+C会复制信息条目标题

18. Bugfix: URLs with percent encoding not correctly decoded while indexing/searching  
    修正：使用%号编码的URLs在索引/搜索中不正确解码的问题

19. Bugfix: Edit - Find/replace not working with empty strings  
    修正：【编辑 - 查找/替换】中空白字符无效的问题

20. Bugfix: pasting HTML content from Chrome web browser makes redundant  tags as a complete html frame was copied in addition to the selected contents  
    修正：从Chrome浏览器中复制后，粘贴内容中包含多余HTML标签的问题。

21. Bugfix: Capture - Import files as child items, it may fail to import accompanying images in sub-directories containing special characters  
    修正：【导入 - 导入文档作为子项】中如果图片所在文件夹含有特殊符号导致导入失败的问题

22. Bugfix: certain dialog boxes not activated when a secondary dialog box exits; This usually happened after picking files or folders  
    修正：某些情况下对话框显示的问题

23. Bugfix: Copy link address not working on Mac  
    修正：Mac中复制链接的问题

24. Bugfix: in the Undelete items dialog box, the 'trash' icon not shown correctly in the description  
    修正：恢复删除项中trash图标显示不正确的问题

25. Bugfix: current changes in HTML editor not precedingly saved before performing export-sepcific operations; Almost all exporting plugins grab data from storage instead of the view components  
    修正：

26. JSAPI: CByteArray::percentEncode(), percentDecode(), saveToFile(), CLocalFile::writeBytes(), platform.formatDateTime(), CNyfDb::applyRelativePath(), evalRelativePath(), makeFileLinkWithRelativePath()  
    JSAPI：更新如下JSAPI`CByteArray::percentEncode(), percentDecode(), saveToFile(), CLocalFile::writeBytes(), platform.formatDateTime(), CNyfDb::applyRelativePath(), evalRelativePath(), makeFileLinkWithRelativePath()`

27. Minor fixes/tweaks/changes  
    其他小修正，调整和更新

    ​

## Version 7.0.0 Beta-22
1. Added: the 'Character set' option for non-Unicode circumstances e.g. Sorting text by Chinese/PinYin, Resolving gibberish characters  
   增加：“字符集编码”选项  
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-12-31_205415.png"  width="70%" height="70%" />

2. Added: a tab widget for the advanced search form and saved searches list in the separate panes  
   增加：高级搜索加人【已存搜索项】  

3. Added: the mouse wheel scroll-up/down action to zoom in/out content in the HTML editor  
   增加：可以使用鼠标滚轮放大和缩小信息条目编辑区内容  

4. Added: the 'Format brush' feature which enables to handily apply text style from current selection to another part of text contents, like using a paint brush; A mouse click on the 'Format brush' tool button to use it once, double-click to keep it active  
   增加：【格式刷】功能  

5. Added: an option to enable using file system icons for outline items (the drive icon for root items, folder icon for branches and file icon for leaf items); Or the default/inbuilt 'cube' icon is selected for info items loading from the image file './images/ico_infoitem.png'  
   增加：可使用系统图标的选项  

6. Added: support of cross-database hyperlinks, which allows to make hyperlinks to info items saved in different .nyf databases; It's required to first have target databases open before making cross-db hyperlinks  
   增加：跨数据库链接  

7. Added: backward compatibility for hyperlinks created within earlier version 5.x  
   增加：兼容v5.x版本的超链接  

8. Added: an indicator icon for info items being loaded as Image gallery  
   增加：在大纲条目加入图片浏览指示标记  

9. Added: support of boolean operators (AND, OR) for searching labels  
   增加：在【高级搜索】中对标签加人AND, OR布尔操作符的支持  

10. Added: support of boolean operators (AND, OR, NOT) for searching partial words  
    增加：对【查找不完整单词】加人AND, OR, NOT布尔操作符的支持  

11. Added: an option to search currently selected branches in the Advanced Search pane  
    增加：在【高级搜索】中加人“当前分支”选项  

12. Plugin: File - Maintenance - Merge database, for merging newer revisions from a specified .nyf database into the current database  
    插件：新增【文件】-【维护】-【合并数据库】

13. Enhancement: an option to display colorful labels; The color is extracted from the associated custom icons  
    增强：可自定义标签颜色，颜色从自定义图标中获取  

14. Enhancement: ability to save/restore the list header of the attachments/results views  
    增强：附件窗口和搜索结果窗口表头的保存和恢复  

15. Enhancement: handle Chinese characters in search phrases with Find-as-you-type  
    增强：即时搜索中加强对中文的处理  

16. Enhancement: new algorithm to allocate unique IDs for each info items, to help the DB-Merge utility to resolve/avoid conflicts  
    增强：为实现【合并数据库】功能做的节点唯一ID算法上的增强  

17. Enhancement: graphical presentation of calendar date and reminder with in the outline view  
    增强：如果信息条目有关联日历，则在大纲视图中将有显示。  
    <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2016-04-01_211044.png"  width="30%" height="30%" />

18. Enhancement: in the hyperink eidting dialog box, bookmarks will be listed in a separate window, that substitutes for the popup menu, as menu items scrolls up/down slower;  
    增强：【编辑链接】中，修改添加书签的呈现方式  

19. Bugfix: v5.x legacy hyperlinks not working  
    修正：v5.x超链接无效的问题  

20. Bugfix: bookmarks not working with new/empty info items  
    修正：书签对于新建和空信息节点无效的问题  

21. Bugfix: corrections to the default focus policy within confirmation popup windows, the 'Yes' button has initial focus for Save-specific operations, and the 'No or Cancel' has initial focus for Deletion-specific operations  
    修正：对话框中默认焦点的优化  

22. Bugfix: shortcuts not working when exporting attachments  
    修正：导出附件时，快捷方式不生效的问题  

23. Bugfix: the plugin 'Export text without formatting' not working  
    修正：导出纯文本插件无效的问题  

24. Bugfix: trashed items may not be listed in Undelete mode if no any other sibling items existing  
    修正：特定情况下删除的节点并未在【恢复删除项】中出现的问题  

25. Bugfix: in the HTML editor, changes not saved when loading image gallery  
    修正：【编辑html源码】时，使用【打开图片浏览】导致html源码不保存的问题  

26. Bugfix: on the main toolbar, shortcut keys not shown in the native format on Mac OS X  
    修正：Mac OS X工具栏中快捷方式的显示问题  

27. Bugfix: defnote/attachments not matched on searching index+labels  
    修正：搜索的一个不匹配的问题  

28. Bugfix: in the image gallery mode, screen may flash when switching over to another picture  
    修正：【打开图片浏览】图片闪烁的问题  

29. Bugfix: in the image gallery mode, no more than 12 images shown in the left side bar  
    修正：【打开图片浏览】多于12张图片的显示问题  

30. Bugfix: in the hyperlink editing dialog box, the OK button is not enabled after editing the hyperlink  
    修正：【编辑链接】中，修改链接后，OK按钮不可用的问题  

31. Bugfix: in the HTML editor, pasting plain text containing special characters (U+0085, U+2028, U+2029) not working  
    修正：【编辑html源码】中，某些特殊字符无效的问题  

32. Minor fixes/tweaks/changes  
    其他小修正，调整和更新


## Version 7.0.0 Beta-21
1. Plugin: Custom search scope  
   插件：增加【搜索 -> 搜索选定范围】  
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_110754.png"  width="50%" height="50%" />

2. Plugin: Custom page margin  
   插件：增加【段落 -> 定制页面边距】  
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-21_084433.png"  width="70%" height="70%" />

3. Plugin: Open folder location of shortcuts  
   插件：对附件快捷方式增加【打开源文件夹】功能  
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_111252.png"  width="60%" height="60%" />

4. Improvement: enabled to open attached documents externally with the original file names  
   增强：当用外部程序打开附件时使用附件原来的文件名

5. Improvement: Options to customize default paragraph attributes  
   增强：自定义默认段落属性  
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-19_111541.png"  width="80%" height="80%" />

6. Improvement: enabled to center an info item on opening from the Query-results or Item-links pane  
   增强：搜索结果的显示方式。

7. Improvement: enabled the outline to auto-scroll when dragging info items over the edge of the view  
   增强：拖动节点到边界时会自动滚屏。

8. Improvement: allows to drag Query results and drop into the outline view, to make item links  
   增强：把条目从查询结果中拖入内容区域将生成相应条目链接。

9. Improvement: allows to customize the main menu bar; Sub menus can be put onto the main menu bar  
   增强：支持自定义菜单    
   <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-12-03_232110.png"  width="80%" height="80%" />

10. Improvement: for Windows, the keyboard_shortcuts.ini can be preserved while re-installing; for Linux/Mac, the keyboard shortcut settings will be saved in the user's HOME directory  
    增强：Windows下keyboard_shortcuts.ini配置文件在安装myBase时可以选择保留。Linux/Mac下键盘快捷方式配置将保存在用户HOME目录。

11. Improvement: for Linux/Mac, the config file (.myBase7.ini) will be saved in the user's HOME directory, so all the configurations can be retained when reinstalling later versions  
    增强：Linux/Mac下，配置文件.myBase7.ini将被保留在用户HOME目录，升级软件将会保留此配置文件。

12. Improvement: for Mac, the new UI style is applied to the main tool bar and tool buttons  
    增强：Mac下全新的UI风格。

13. Added: the 'Add info items' menu item within the Lable/Calendar view  
    增加：在【日历】和【标签】视图加入“添加条目”  
    <img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-10-21_083540.png"  width="70%" height="70%" />

14. Added: the new logo image file  
    增加：全新设计的logo图片

15. Added: the option to customize directory path to save index/backup files  
    增加：自定义index/backup的目录，【查看】->【选项】->【查找】和【查看】->【选项】->【备份】

16. Bugfix: The Ctrl+Open hotkey accidentally causes the database to lock as Readonly  
    修正：Ctrl+Open热键导致把数据库变成只读的问题

17. Bugfix: The program may crash when the 'Find as you type' action re-enters  
    修正：“键入时搜索”有可能出现crash的问题

18. Bugfix: garbage characters may appear in the Revision History list on non-English platforms  
    修正：修正在非英文操作系统下【历史修订版本】中文字显示乱码的问题

19. Bugfix: the default icons not imported on creating new databases  
    修正：修正新建数据库文件时默认未包含默认图标的问题

20. Bugfix: the program may crash on Mac when pressing Close button while a popu menu is active  
    修正：Mac下有可能出现crash的问题

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

2. Tool button: 'Insert attachment link ...', with multi-selection enabled  
   添加工具栏“插入附件链接”，支持多选批量插入

3. Allow to copy/paste cells/rows/tables from MS-Excel  
   支持从MS-Excel复制表格，行。

4. Auto-import linked images (if any) when copying HTML contents from MS-Word  
   复制MS-Word里html内容时自动导入带链接的图片

5. Fix: ignore duplicate image links when copying online HTML contents  
   修正：复制html时忽略相同图片链接的问题。

6. Bugfix: backslashes not working when copying HTML content  
   修正：复制html时，反斜杠（\）不生效的问题。

7. Bugfix: hyperlinks to local files (e.g. file:///d:/dir/...) may not work  
   修正：到本地文件链接 (e.g. file:///d:/dir/...)不生效的问题。

8. Bugfix: custom icons' label text not replicated while replicating database  
   修正：复制数据库时自定义图标名称丢失的问题。

9. JSAPI bindings for MS-Word (Windows)  
   MS-Word与JSAPI的绑定（Windows版）

10. Export MS-Word outline (Windows)  
    导出MS-Word大纲（Windows版）

11. Import MS-Word outline (Windows)  
    导入MS-Word大纲（Windows版）

12. Bugfix: a bug in the HTML document parser with self-closing HTML elements may cause the program to crash during indexing/searching  
    修正：索引，搜索时崩溃的问题

13. Bugfix: custom text styles (bold/italic/underline) not working for new item content  
    修正：自定义文字格式（加粗，斜体，下划线）在新条目内容不生效的问题

14. Show item titles on the status-bar during indexing  
    搜索时状态条线索当前条目的标题

15. Workaround: within the inbuilt HTML editor, Text Input Method not working well on dark backgrounds (HSV:V<128)  
    在HTML编辑器里，由于背景为深色不显示输入内容的问题

16. Added the Capture/Share menus; The Capture menu contains 'Import ...' specific utilities, while the Share menu contains 'Export ...' specific utilities  
    加入 捕获 和 分享 菜单

17. Plugin: Tools - Reveal internal data, which allows to view and modify internal data files; Do not modify internal data files by hand unless you have to fix broken links  
    增加 工具 - 内部链接数据 工具

18. Enabled clipboard monitor to download linked images when copying web contents from web browsers or MS-Word  
    剪贴板监视加入图片下载支持

19. Enabled clipboard monitor to copy contents from MS-Word/Excel including tables/cells/images  
    剪贴板监视加入从 MS-Word/Excel复制表格图片的支持

20. Added the Paragraph menu, which contains the paragraph specific formatting utilities  
    加入段落菜单（包含段落相关设置的工具）

21. Added: Paragraph - Single line spacing, One and half line spacing and Double line spacing  
    加入 段落 - 单倍行距，1.5倍行距，2倍行距

22. Bugfix: line-spacing not working well with multiple paragraphs selected  
    修正：行间距在多段选择时的问题


## Version 7.0.0 Beta-18 ##
1. WebCollect addon for Mozilla Firefox  
   用于Firefox浏览器的WebCollect插件

2. WebCollect addon for Google Chrome  
   用于Google Chrome浏览器的WebCollect插件

3. Context menu: Copy image  
   复制图片

4. Context menu: Copy image URL  
   实用工具（图片）：复制图片链接

5. Context menu: Save image as  
   实用工具（图片）：图片另存为

6. Context menu: Resize image  
   实用工具（图片）：图片尺寸

7. Context menu: Rotate image  
   实用工具（图片）：旋转图片

8. Auto-download linked images (if any) when copying HTML content from web browsers  
   从浏览器复制html内容时，自动下载链接图片

9. Auto-grab linked images (if any) when copying HTML content from MSWord  
   从word复制html内容时自动获取链接图片

10. Drag-drop embedded images into the attachment list to save the image data as attachments  
    把html里嵌入的图片拖到附件栏，会以附件形式保存图片

11. Drag-drop attached png/jpg/gif/bmp files into HTML editor to insert the images into HTML content  
    拖图片附件png/jpg/gif/bmp进html编辑器，即可插入图片

12. Drag-drop non-graphic attachments into HTML editor to insert hyperlinks  
    拖非图片附件进html编辑器，即可插入链接

13. Drag-drop info items into HTML editor to make hyperlinks; The CTRL key modifier is needed to be held down while dragging info items into current item content  
    按ctrl按钮的同时，把条目拖到html编辑器即插入链接。

14. Support of hyperlinks to attachments stored in either current or any other info items; Clicking on a hyperlink triggers the linked attachment to be open externally with the associated program  
    在编辑链接框中，通过“插入附件链接”菜单，支持链接到任意节点的附件链接。

15. Edit - Text Utilities: Make selected text fields into HTML table  
    编辑 - 实用工具（文本）：转换文本为表格

16. Edit - Text Utilities: Make selected text upper/lower case  
    编辑 - 实用工具（文本）：转换为大写，小写字母

17. Edit - Text Utilities: Sort selected text lines  
    编辑 - 实用工具（文本）：文本行排序

18. Edit - Text Utilities: Remove unwanted spaces from selected text  
    编辑 - 实用工具（文本）：清除多余空白

19. Customizable zoom level for tool buttons, so it can work with high resolution monitors  
    增加“工具按钮显示缩放系数”，可以调高系数便与在高分辨率屏幕上使用

20. Display a lighter text in database Tabs with unified title bar on Mac  
    改进Mac系统上文字显示

21. Substituted inbuilt file parser for external txt/htm DLLs to parse text/html content during indexing and searching  
    使在索引和搜索时使用用自带dll分析。

22. Added the monthly calendar view  
    添加日历月视图

23. Drag-drop .nyf file into main window to be open as database  
    当把.nyf文件拖到主窗口将会打开此数据库文件

24. Syntax highlighter for html source  
    编辑html源代码语法高亮

25. Save and restore toolbar position  
    保存，恢复工具栏位置