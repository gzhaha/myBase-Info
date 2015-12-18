# myBase 7.x Javascript APIs Reference
返回[myBase-Info首页](https://github.com/gzhaha/myBase-Info)  

官网相关链接如下(Official website)：
[http://www.wjjsoft.com/mybase_v7_jsapi.html](http://www.wjjsoft.com/mybase_v7_jsapi.html)

> **注意：**
> 以下仅为**个人翻译版，均为个人理解**。如对本翻译版本有疑问，请以官网内容为准并自行查阅以上官网相关内容。
> **The below translation is based on my personal understanding, always refer to the official website in case of any confusion.**

## Introducing myBase Javascript APIs
myBase has integrated the Javascript engine, and exposes a set of plugin API in Javascript; With the plugin API, you can write your own plugins (scripts) to manipulate information stored in your .nyf databases and perform particular tasks.  

myBase 7.x 集成了Javascript引擎和提供了一套API插件接口。通过API插件，可以方便的自行编写插件脚本处理.nyf数据库的内容和实现特定任务。  

## Writting Plugins in Javascript（使用Javascript编写插件）
Writting myBase plugins in Javascript is simple. Just write source code using a text editor (e.g. Windows Notepad), and save it as a *.js file within the ./plugins subfolder under myBase setup folder, and then re-launch myBase for new plugins to be registered and shown in menus. Following are the sample code snippets.  

编写myBase插件并不复杂。只需要使用文本编辑器（如：写字板）编写源码，保存成.js文件并存在安装目录的./plugins下，然后关闭并重新启动myBase软件即可，新的插件会出现在相应的菜单中。以下提供了一些简单的示例源码。


    //DEMO #1: Display the About info;
	//显示“关于”信息
    alert(about());
    
    //DEMO #2: add a file as attachment in the currently info item;
	//把一个文件加入当前信息条目的附件
    var nyf=new CNyfDb(-1);
    var sFn=platform.getOpenFileName({sTitle: 'Add a file', sFilter: 'Text files(*.txt);;All files(*.*)'});
    if(sFn){
    	var nBytes=nyf.createFile(plugin.getCurInfoItem()+'/'+'newfile.txt', sFn);
    	if(nBytes>=0){
    		plugin.refreshDocViews(-1);
    		alert('File added.');
    	}
    }
    
    //DEMO #3: Load a specified .nyf database, traverse the outline tree and show the item titles with indentation;
    var sFn=platform.getOpenFileName({sTitle: 'Open file', sFilter: 'nyf files(*.nyf);;all files(*.*)'});
    var nyf=new CNyfDb(sFn, false), sTxt='';
    nyf.traverseOutline('/Organizer/data/', false, function(sPath, iLevel){
    	var sHint=nyf.getFolderHint(sPath);
    	if(sHint=='') sHint='new item ...'; else if(sHint==undefined) sHint='secured item ...';
    	var sIndent=''; while(iLevel-->0) sIndent+='\t';
    	sTxt+=(sIndent+sHint+'\n');
    });
    alert(sTxt);
    
    //DEMO #4: Use the currently working .nyf database, and display the current item's HTML content;
	//显示当前节点的html源码
    var nyf=new CNyfDb(-1);
    var f=new CLocalFile(plugin.getCurInfoItem(), '_~_~_notes.html');
    var sHtml=nyf.loadText(f);
    alert(sHtml);
    var sTxt=platform.parseFile(sHtml);
    alert(sTxt);


The word 'JavaScript' may bring to mind features such as event handlers (like onclick), DOM objects, window.open, and getElementById. But within myBase Javascript APIs, there're no such interfaces at all. myBase exposes a set of application specific classes, objects and functions, such as the 'plugin' and 'platform' objects. In addition, myBase exposes several other classes, such as 'CNyfDb', 'CLocalFile', 'CLocalDir', and 'CAppWord' for manipulating .nyf databases and local files, and exchanging data with Microsoft Office.   

通常JavaScript意味着一些诸如事件处理（按键时），DOM组件，window.open或者getElementById的功能，但myBase API并不提供这类接口。myBase API只提供一些与应用相关的类，组件和接口，例如“插件”和“平台”接口。另外，myBase API亦提供了'CNyfDb', 'CLocalFile', 'CLocalDir', and 'CAppWord'类，通过这些类，可以实现和myBase数据库引擎的通信、操作本地文件以及和Microsoft Office交换数据。 

## Installing .js Plugins（安装js插件）
myBase loads .js plugins by default from the './plugins' sub directory under the program's installation directory. You have the convenience of installing .js plugins by simply putting .js plugin files to the './plugins' directory, and then re-launch myBase to let new plugins to be registered and listed in the menus or on the toolbar.  
默认情况下，myBase启动时会从安装目录的./plugins文件夹载入.js插件。您只需把.js文件复制到./plugins目录，然后重新启动软件即可。 

In addition, myBase supports loading plugins from multiple directories; To customize the plugin directories, please try to edit the myBase.ini config file by using a plain text editor (e.g. notepad.exe) at the line below; Multiple directories are separated with a semicolon.  
另外myBase也支持从多个目录载入插件，可以通过修改myBase.ini配置文件中的App.Path.PluginFiles=自定义这些目录，多个目录之间通过**分号**分隔，示例如下。

    App.Path.PluginFiles=./plugins;/home/username/mybase/plugins1;/home/username/mybase/plugins2

In order for your plugin script to be registered and installed in menus or on toolbars, a file header must be inserted in front of your functional script code within the .js file; The file header describes the plugin script and defines a few values to determine how/where to install it.  
在每个.js插件文件的开头，都必须加入用来定义/标识插件的几行文件头文字。有了这些内容，.js文件才会被软件正确识别和加载。

The file header consists of a couple of [name=value] entries. Here's a sample header.  
请看如下示例： 

    //sValidation=nyfjs
    //sCaption=Custom text indent ...
    //sHint=Custom indent for selected paragraphs
    //sCategory=MainMenu.Paragraph
    //sPosition=Par-99
    //sCondition=CURDB; DBRW; CURINFOITEM; HTMLEDIT
    //sID=p.CustomTextIndent
    //sAppVerMin=7.0
    //sShortcutKey=
    //sAuthor=wjjsoft
    
    // Your functional script code go here ...
    alert('Hello world');

* sValidation: The '//sValidation=nyfjs' header must be kept in each .js plugin files as it is (hard-coded);
每个.js插件**必须**包含//sValidation=nyfjs在开头
* sCaption: the plugin's caption text, shown in the menu or on the tool button;
插件名称，将显示在菜单
* sHint: the descriptive text about the plugin functionality, shown on the status bar when the menu item is hovered;
插件描述，将显示在状态栏（当选中插件时）
* sCategory: specifies in which menu or toolbar to put the plugin item; it can be 'MainMenu.[\*\*\*]', or 'Context.[\*\*\*]', and or 'ToolBar.[\*\*\*]', where '[\*\*\*]' is a menu/toolbar's tag name (English, not localized names);
指定插件在那个目录或者工具条出现，可以设置为'MainMenu.[\*\*\*]'或者'Context.[\*\*\*]'或者'ToolBar.[\*\*\*]，'[\*\*\*]'为menu/toolbar下的下级名称
* sPosition: specifies a tag in alphabetical order for positioning the plugin item inside the target menu or toolbar;
插件显示顺序
* sCondition: specifies in which conditions are required for the plugin to function normally, can be one of the following values; 
指定在何种情况下插件可选
    * CURDB: the current database must be open and accessible;
当前数据库可打开和读取时
    * DBRW: the current database must be read/writeable;
当前数据库可被读写时
    * CURINFOITEM: the current info item must be available and accessible;
当前节点可被读取时
    * HTMLEDIT: the current HTML content must be editable;
当前节点可以被编辑时
    * OUTLINE: the outline pane must be visible and active (focused);
大纲可见和激活时
    * HTMLSELECTED: the HTML content is currently active (focused) or has text content selected;
选中节点内容时
    * TABLE: the input caret must be put in a &lt;table&gt; section in the HTML content;
光标在表格时
* sID: a tag to identify the plugin item; it's also used for localization of messages and plugin icons;
插件标签，亦用于本地化语言和指定插件图标

## A Simple Way to Test Script Code （测试脚本的简单方法）
myBase provides a simple way to test your script code, without having to writting script code in .js files, you can simply write script code in the inbuilt HTML editor, and then highlight the script code, and select the [Tools - Evaluate expression or js code] menu item to run it. If the script code (e.g. math expression) returns a value that is not 'undefined' or empty string, it will be inserted into the HTML content as a result of the math expression.   

myBase提供了一个简单的方法测试脚本代码，你可在信息节点内写入代码，然后选中这些代码，选择【工具->计算表达式或执行js脚本】来运行这些选中的代码。  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/2015-12-18_133548.png"  width="60%" height="60%" />

## Concepts & Terms （基本概念和用语）
To help quickly get started with myBase Javascript APIs, please read about the following concepts and terms at first.  
要想快速了解myBase Javascript APIs，建议先阅读以下基本概念和用语。
1. SSG: stands for the structured storage library on which myBase is built.
指myBase基于的数据库引擎。
1. Database: stands for myBase .nyf databases.
指myBase的nyf数据库。 
1. SSG path: reference to file/folder entries in .nyf databases; it works like file system on hard disk.
 用来指向.nyf数据库里的文件夹或文件，和硬盘的文件系统相类似。 
1. SSG file: stands for a file-like entry (e.g. attachment) in .nyf databases, and is referred by SSG file path (e.g. /organizer/data/1/2/3/abc.txt).
代表.nyf数据库里的每个条目，使用SSG file path作为指向（如：/organizer/data/1/2/3/abc.txt）。 
1. SSG folder: stands for a folder-like entry (e.g. info item) in .nyf databases, and is referred by SSG folder path (e.g. /organizer/data/1/2/3/).
代表.nyf数据库中类似**文件夹**的条目（如：信息节点），使用SSG folder path来指定（如：/organizer/data/1/2/3/）
1. SSG entry: stands for either a file or folder entry.
代表文件或文件夹
1. Nyf root path: SSG path to the container of all top-level info items in .nyf databases; it is hard-coded as '/Organizer/data';
SSG的根路径，包含.nyf根信息节点，**必须**为'/Organizer/data'
1. AppDataOfEntry: each SSG file/folder entry maintains a list of application-defined data (Integers).
每个SSG文件和目录的应用相关数据
1. platform object: provides a set of API which wraps system specific functions.
提供一些系统相关的API
1. plugin object: provides a set of API which wraps myBase plugin API, for accessing selected content in views or controlling the main program.
提供API用于访问当前视图中选中的内容或者程序
1. CNyfDb class: provides a set of API which wraps the SSG structured storage library, for accessing to files/folders within .nyf databases by using SSG paths.
提供API用于访问nyf数据库中的文件和目录
1. CLocalFile class: provides a set of API for accessing to local files.
提供API用于访问本地文件
1. CLocalDir class: provides a set of API for accessing to local directories.
提供API用于访问本地文件夹
1. CAppWord classes: provides a set of API for controlling MS-Word by using OLE-Automation.
提供API用于控制MS-Word。

## The Global Functions Reference （全局函数参考）
The global functions (e.g. alert, confirm, input, etc.) can be called directly without preceding instantiation or initialization.  
**about**
The 'about' function returns the application information, such as program title, version, copyright notice, etc.;  
'about'函数返回程序相关信息，包含程序名称，版本，版权等信息。 

- Prototype: about();
- Parameters: None
- Return Value: String;
- Example: var s=about(); alert(s);

**alert**
