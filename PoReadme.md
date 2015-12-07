# 一、特例，保持原文: #

```
msgid "Since: 2.4"
msgstr "Since: 2.4"
```
```
msgid "Since: 3.0"
msgstr "Since: 3.0"
```
```
msgid "@See_also: #GtkVBox"
msgstr "@See_also: #GtkVBox"
```

# 二、带格式条目，保持原格式： #

包含几种情况：

## 第1种： ##

凡是msgid内容中包含"xxx: yyy"这种格式的，对于"yyy"之前的内容"xxx: "不翻译。
(半角的":"及空格请保留, 像"Returns: " 也不能翻译成"返回:")。

```
msgid "@widget: the object which received the signal."
msgstr "@widget: 接收信号的对象。"
```
#这里的"@widget: " 不翻译，请保持原格式，包括":"号和" "空格。

```
msgid "@rgba: (out): a #GdkRGBA to fill in with the current color"
msgstr "@rgba: (out): 一个使用当前颜色填充的 #GdkRGBA 对象"
```
#这里的"@rgba: (out): " 不翻译，请保持原格式，包括":"号和" "空格。

```
msgid "@Short_description: A button to launch a color selection dialog"
msgstr "@Short_description: 打开颜色选择对话框的按钮。"
```
#这里的"@Short\_description: " 不翻译，请保持原格式，包括":"号和" "空格。

```
msgid "Returns: a new color button"
msgstr "Returns: 一个颜色按钮控件"  
```
#这里的"Returns: " 不翻译，请保持原格式，包括":"号和" "空格。

总之，记住一句话：凡是msgid以一些字符开始，后面跟": "的，请保持最后一个": "前的内容不变。

## 第2种： ##

在内容中出现"#"、"@"、"%"等字符前导的单词/非单词，请保持原样，并在前后留半角空格" "。例如：

```
msgid "Creates a new #GtkHBox."
msgstr "新建一个 #GtkHBox 。"
```
#保持" #GtkHBox "不翻译，并前后留半角空格(如果位于结尾部分，后面再无字符的情况，可以省略掉后面的空格)。

```
msgid "@homogeneous: %TRUE if all children are to be given equal space allotments."
msgstr "@homogeneous: %TRUE 则所有子控件都分配相同的空间大小。"
```
#保持"%TRUE"不翻译，并前后留半角空格。