# Write a myBase 7.x Plugin in 4 Steps
Writing myBase 7.x plugin is simple and easy. You do not need complicated algorithms to make simple plugins but some basic **javascript** knowledge.  

You can access to all the examples and API technical documents via [Official Website](http://www.wjjsoft.com/mybase_v7_jsapi.html), or [API中文版(翻译缓慢进行中)](https://www.gitbook.com/book/gzhaha/mybase-7-javascript-apis-reference-cn/details).  

Below example shows how to achieve the function of setting background image for specific info item.

## Step 1: Copy below code to a text file and save as XXX.js (XXX is your Plugin file name)
```
//sValidation=nyfjs
//sCaption=XXXXXXXXXXXX
//sHint=XXXXXXXXXXX
//sCategory=Context.HtmlEdit
//sPosition=ZZ-255
//sCondition=CURDB; DBRW; CURINFOITEM; HTMLEDIT
//sID=p.XXXXXXXXXXX.SetBgImg
//sAppVerMin=7.0
//sShortcutKey=
//sAuthor=Your name

/////////////////////////////////////////////////////////////////////
// Extension scripts for myBase Desktop v7.x
// Copyright XXXXXXXXXXX
/////////////////////////////////////////////////////////////////////

var _lc=function(sTag, sDef){return plugin.getLocaleMsg(sTag, sDef);};
var _lc2=function(sTag, sDef){return _lc(plugin.getLocaleID()+'.'+sTag, sDef);};

var _trim=function(s){return (s||'').replace(/^\s+|\s+$/g, '');};
var _trim_cr=function(s){return (s||'').replace(/\r+$/g, '');};

try{
	var xNyf=new CNyfDb(-1);
	if(xNyf.isOpen()){
		if(!xNyf.isReadonly()){
			if(plugin.isContentEditable()){
				//your code Below 下方开始加入代码





				
				}

			}else{
				alert(_lc('Prompt.Warn.ReadonlyContent', 'Cannot modify the content opened as Readonly.'));
			}
		}else{
			alert(_lc('Prompt.Warn.ReadonlyDb', 'Cannot modify the database opened as Readonly.'));
		}
	}else{
		alert(_lc('Prompt.Warn.NoDbOpened', 'No database is currently opened.'));
	}
}catch(e){
	alert(e);
}

```

## Step 2: Define all the XXXXXXXXXXX in the source code
For example: //sCaption=XXXXXXXXXXXX, you can change XXXXXXXXXXXX to Caption name of the plugin.  

Refer to [Official Website](http://www.wjjsoft.com/mybase_v7_jsapi.html#install) for more details.  

## Step 3: Writing Code
There are more than one way to do this, below is one simple and direct way written in eight lines of codes.
```
				var sTxt = prompt('Background Img name:', '', 'Enter Background Img name');
				if (sTxt){
					var sCon = plugin.getTextContent(-1, true);
					var regx = /<body(.*?|)>/;
					var html = sCon.replace(regx, '<body background="'+ sTxt + '">');						
					plugin.setTextContent(-1, html, true);						
					plugin.setDomDirty(-1, true);
					plugin.commitCurrentChanges(-1);					
				}	
```
The first line will ask user to input the desired background image name from user (image file already been put to the attachment of the specific info item) and assign to variable "sTxt". You can find more information about function 【prompt】 via [API document - prompt](http://www.wjjsoft.com/mybase_v7_jsapi.html#prompt).  

Then "if" statement will be used to see if user input anything, if "yes", the following codes will be run.  

The third line will get the info item's html source code and assign to variable "sCon". You can find more information about plugin object 【plugin.getTextContent】 via [API document - plugin.getTextContent](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_getTextContent).  

The forth line defines a regular expression rule.  

The fifth line add the background img information to the html source code.  

The sixth line assigns the changed html source code back to the info item. You can fine more informaion about 【plugin.setTextContent】via [API document - plugin.setTextContent](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_setTextContent).  

The last two lines are used to commit changes. Information about 【plugin.setDomDirty】 and 【plugin.commitCurrentChanges】 via [API document - plugin.setDomDirty](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_setDomDirty) and [API document - plugin.commitCurrentChanges](http://www.wjjsoft.com/mybase_v7_jsapi.html#plugin_commitCurrentChanges).  

## Step 4: Use the plugin
Save the XXX.js file under myBase plugin folder. Exit myBase, then run myBase again. Refer to [Official Website](http://www.wjjsoft.com/mybase_v7_jsapi.html#install) for more details on how to install plugin.  

The plugin will be loaded and you can run as below:  
<img src="https://raw.githubusercontent.com/gzhaha/myBase-Info/master/images/plugineg1.gif"  width="60%" height="60%" />  

A working copy of the plugin could be found [Here](https://github.com/gzhaha/myBase-Plugins/tree/master/plugins#7-setbackgroundimgjs).

## Future Enhancements of this plugin
As you already experienced, this plugin is simple and some improvemnets can be done to make this plugin more convenience.  

For example:

* Try to get the attachment file names and display using dropdown box. With this enhancement, user no longer need to enter the image file name manually. (By searching the API document, you will know how to do this ^_^)

* Add a function to restore to default.

* ...  

