# 项目简介 #
> 最初申请这个项目的想法是打算将gtk+的API文档汉化（曾在linuxfans、linuxsir上发贴倡仪）。开始打算翻译经过预编译的docbook形式的文档(sgml/xml)，经过公社的KDE和cavendish等人指正，发现用这种方式翻译的话问题很多，如：
  1. 翻译工作量大
  1. 不能及时跟进最新版本
  1. 如果要翻译后续版本，那么以前的翻译成果很难继承
  1. ......
> 由于这些问题无法完美解决，于是项目暂停。后来尝试用getpo和xmlpo工具将其转换为po文件进行翻译，但这些工具并不能正常处理用gtkdoc产生的xml文件， 于是根据gtkdoc文件格式自己写了一个工具来转换源文件中的文档到pot文件，并将翻译完成的po文件还原到源文件中. 这个工具现在已经开始工作，你可以从http://gtk-doc-cn.googlecode.com/svn/trunk/tools/gtkdocpo 免费获得。

> 有了gtkdocpo之后，一切都变得简单起来。因为我们可以用 **翻译po文件的方式来翻译文档** ，而且我们不仅可以翻译gtk+文件，而且可以翻译gnome的其它开发工具的文档，只要它使用了gtkdoc来产生，当然翻译的语言也不仅仅局限于简体中文了，即使使用其它语言的用户也可以方便地将这些文档进行本地化，还有一点，翻译以后的文档和原始的英文文档排版上没有任何差别，也可以使用你的devhelp来浏览它们。

> 做为一个示例，我们翻译了libgksu的文档(翻译质量不一定高)，你可以通过以下地址查看这些文件：

pot文件：http://gtk-doc-cn.googlecode.com/svn/trunk/projects/libgksu/libgksu-2.0.0.pot

简体中文po文件:http://gtk-doc-cn.googlecode.com/svn/trunk/zh_CN/libgksu/libgksu-2.0.0.po

简体中文libgksu API文档：http://gtk-doc-cn.googlecode.com/svn/trunk/zh_CN/libgksu/html-2.0.0/index.html

作为对比，你可以在这里看到英文文档：http://people.debian.org/~kov/gksu/reference/

如果你希望在你的devhelp中看到简体中文，那么就参与进来吧，我们一起翻译它们， :)。

# 如何加入 #

我们的项目采用googlecode管理，并开设了简体中文的邮件列表:

http://groups.google.com/group/gtk-doc-cn

请申请加入此邮件列表，我们的管理员会将你加入项目组中，这样你就可以使用svn来下载/提交po文件。

# svn目录结构 #

在使用svn之前， 请先了解一下我们项目的目录结构。
我们主要的工作目前在trunk分支进行(其它分支以后也许会用到)：
http://gtk-doc-cn.googlecode.com/svn/trunk

```
tools/              (工具目录)
  |--credits.xml    (发布文档时本项目加入的版权信息)
  |--gtkdocpo       (制作pot及合成到源码的主要工具)

projects/           (项目文档目录,包含不同项目的文档模板及pot文件)
  |--glib/
  |    |--glib-VERSION.pot      (某版本的pot文件)
  |    |--docs-VERSION/         (某版本的模板文件)
  |--gtk+/  
  |    |--gtk-VERSION.pot
  |    |--gdk-VERSION.pot  
  |    |--gdk-pixbuf-VERSION.pot  
  |    |--docs-VERSION/  
  |        |--gtk/
  |        |--gdk/  
  |        |--gdk-pixbuf/  
  |--libgksu/
  |    |--libgksu-VERSION.pot
  |    |--docs-VERSION.pot
  |......           (以后将陆续加入其它项目)

zh_CN/              (简体中文语言目录，包含不同项目的待翻译文件,翻译者只需取出本目录下的内容)
  |--message.mo     (已翻译的文档词条总汇，用于poedit中生成词库，以便使用自动翻译功能)
  |--libgksu/
  |    |--html-VERSION/         (某版本的简体中文用户文档, 最终发布形式)
  |    |--docs-VERSION/         (某版本的文档模板,需要翻译)
  |    |--libgksu-VERSION.po    (某版本的libgksu的po文件，需要翻译)
  |    |-- ......
  |--gtk/
  |    |--html-VERSION/
  |    |--tmpl-VERSION/
  |    |--gtk-VERSION.po
  |    |--....
  |......
......  (以后可能加入其它语言，如zh_TW等)
```

# 怎样开始翻译 #

(在翻译之前请先确认你已为本项目组成员, 否则你无法提交)

如上所示目录结构，如果你只是翻译，那么你可以取出要翻译的全部简体中文内容：

svn checkout https://gtk-doc-cn.googlecode.com/svn/trunk/zh_CN gtk-doc-cn --username

或者你只想翻译其中的某份文档（如libgksu）,那么你也可以只取出libgksu的内容：

svn checkout https://gtk-doc-cn.googlecode.com/svn/trunk/zh_CN/libgksu --username


# 如何翻译 #

Add your content here.  Format your content with:
  * Text in **bold** or _italic_
  * Headings, paragraphs, and lists
  * Automatic links to other wiki pages
















