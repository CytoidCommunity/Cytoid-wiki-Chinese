目前有两个Cytoid预览器，两者都只适用于Windows。

它们是：

- TigerHix的Cytoid Player
- Suconh的Cytus 2排行榜球员

这两个软件都可以从[General Resources](https://sites.google.com/site/cytoidcommunity/general-resources)下载。

> 译者注:或许你访问不了这个链接,不过不用担心,群里有这些的链接

本指南介绍如何设置这些预览软件。



# TigerHix的Cytoid Player



要求：

- 你的图表的Wav音频。（您可以使用Audacity来实现此目的）
- 你的谱面本身。
- level.json（与Cytoid相同的格式）
- 背景（.jpg或.png）



优点：

- 支持实时故事板编辑。
- 对C1图表格式的固有支持。

缺点：

- 有时候会有延迟。
- Cytoid UI相当基础。



下载Cytoid Player并单击exe后，然后进行配置，你会发现它......什么都没有！ 

那是因为它没有资源可以演示。

对于初次使用的用户，建议首先执行一次程序，因为它将为您创建文件夹以便放置文件。



![img](https://lh3.googleusercontent.com/QrkiAG7_JV-kEHhWpapn43drUJX9UxpYQO_qK_91kiVZL3Ypmq798gtYU5MEsCRblZ2yy_INBvHR-XQQ2zwHXIdj5xU99PsWLnGBCUIy9Kp2_JlBrCSv=w1175)



打开Windows资源管理器，在地址栏中输入“％appdata％”，不带引号。然后到上一级文件夹。你会看到这些文件夹：



![img](https://lh5.googleusercontent.com/juLphyO89rC_5N_BDAWiVyk1KCAOX0fa0RIE1p9Vk2NS6YL2_PraerBRXnWpfAXzGP79rH-EN5iixZ7w-F-LIPClezrLBo2qVo5Tm6cukNbUgZ2T1XVN=w472)



转到LocalLow> TigerHix> Cytoid

你会看到这些物品。我们感兴趣的是“player”文件夹。如果你还没有运行Cytoid Player一次，很可能没有TigerHix文件夹或Cytoid文件夹，很可能甚至没有这些项目。

如果在运行Cytoid Player一次后没有Player文件夹，则只需创建该文件夹。



![img](https://lh3.googleusercontent.com/XCwh9AaIZn3g-78ZeiSUCdQfbJMYzehXP2Osw6b4XekrWQbFitEtqNIN1_wD1Ik18BiV7gzDo7L8BVHVW0K2zqJgIyLOAvhept5KgSP6gp6eiU8h2Ec=w472)

将您的文件放在此“player”文件夹中。

确保level.json正确引用这些文件。别忘了，**我们在这里使用wav，而不是mp3**。

如果操作正确，您可以在运行Cytoid Player时播放谱面。

注意：storyboard.json也应该在这里制作，放在这里或在这里编辑。只要您对文件进行保存，Cytoid Player就会自动更新故事板的预览。







# Suconh的Cytus 2 Chart Player



设置：

下载Ver.0.7。把它解压到合适的地方。下载Ver.0.8并覆盖解压到ver.0.7的的文件夹。转到文件夹“I”并将里面的文件移动到PlayerDemo.exe所在的文件夹中。

如果您点击PlayerDemo.exe，您将看到suconh制作的酷炫酷谱面。这是一个关于C2格式有多强大的演示（它实际上不是人玩的，所以不要因为它看起来对你来说很难的而沮丧）。

但我们不是来玩Suconh的谱面的。我们希望Chart Player能够播放我们自己的谱面。



要求：

- 你的图表的Wav音频。（使用Audacity转换）
- 你的谱面本身。
- SETTINGS.TXT
- 背景（必须是.png）。
- 徽标/图标（必须为.png，尺寸为512x512）。（您可以简单地关闭suconh的徽标，制作自己的徽标，或者创建一个空白.png）



将您的Wav音频，图表，背景和徽标放入PlayerDemo.exe所在的文件夹中。将其命名为统一的内容，以便您可以轻松跟踪您所拥有的文件。

例如：

- shop.wav（音频）
- shop.json（图表）
- shop_bg.png（背景）
- shop_logo.png（logo）



将settings.txt重命名为简单的内容，以便将来提醒您该文件的设置。

假设这是你第一次，settings.txt很可能是“我通过MXM”的配置，这是suconh的图表。

对我来说，我将其重命名为“settings- [title] .txt”，在这种情况下，它是“settings-I.txt”



打开现在重命名的设置-It文件，复制内部的所有内容，然后转到[https://jsoneditoronline.org/](https://www.google.com/url?q=https%3A%2F%2Fjsoneditoronline.org%2F&sa=D&sntz=1&usg=AFQjCNEg1DlNDixbJtlahsjvW2Qe_QtkKg)。



![img](https://lh6.googleusercontent.com/9B13wiIdPjMKQirAQm1uqRxn1KR5trHOeAS2VUFwx6EweQ5OWqfbGKIJ_D-GV1xzZzm_i38c61e9sgpeFm6et2yTTjoZH4JMTYUGvdv2d2ztaKI6qv3c=w1175)



粘贴到左窗格，然后单击页面中间的右箭头（上面的框）将它们解析到右窗格。

根据需要进行编辑，对于下面的屏幕截图，我使用Bentux的Dizzolve谱面配置。



![img](https://lh4.googleusercontent.com/hFYWbJGZUTstrBvPZGgkchgF0nYhON_fZ0GdQnWA3SG4WBEURANRils1C0zP0qINB6_3pcUpD-9hypNqRoUHfs9vel6zpXMBTbambBXTvc7uiI7wBlg=w1175)



在右窗格中编辑后，您可以使用页面中间的第二个框（向左箭头）向后解析。



![img](https://lh6.googleusercontent.com/zTbxbYOuqDcevzq3pUW9SI7OACPlqHOX8aIueg1E2UYMc01VCimLuZKkGkRIBDtYLFUezOsmAnTYOLaj6NDtD1yOoPXeCJNm3H0LQqgUSmhw7bopBrOx=w1175)



解析后按此按钮删除空格。

现在复制左侧窗格中的所有文本，然后返回到资源管理器窗口。创建settings.txt并将此文本粘贴到该文件。保存。您可以单击PlayerDemo.exe立即播放您的图表。



注意：如果要在C2 Chart Player中使用C1格式，则必须添加`“useOldFormat”:1`。

为此，只需添加它，如下所示：



![img](https://lh6.googleusercontent.com/7_I_35-Cbynh_egS1tbidOsH3mWI_rcSCNW0V8cQcGRW8MmZe1L4WpTHHAluuGCNGEKva3SvVC-WqX4Ip9xEs8ibS02yg4BnlEY38dMjSyglQxTiNps=w1175)