## 如何在Cytoid上游玩谱面？

首先，将您收集并制作的内容放入一个文件中。你应该有这些的文件：

![img](https://github.com/Teages/Cytoid-wiki-Chinese/blob/master/guides/charting/111.png)

它应该是这样的：

（请注意.chart文件不是必需的，它可以是“path”的.txt文件，并且storyboard.json也不是必需的）

- 谱面文件（图中标记为.chart，可以是chart.(name).txt或其他）
- level.json（见下文）
- storyboard.json（不是必需的，参考故事板部分）
- 主要音乐（标记为music.mp3）
- 预览音乐（标记为preview.mp3）
- 背景图片（标记为background.jpg）

之后，选择一切后，压缩。（将所有内容添加到.zip文件中）然后，将.zip扩展名类型更改为.cytoidlevel类型。如果您的计算机不允许您这样做，请参考[此网站](https://www.google.com/url?q=https%3A%2F%2Fwww.thewindowsclub.com%2Fshow-file-extensions-in-windows&sa=D&sntz=1&usg=AFQjCNFzmeNOkOclODSmd2WJ9U3flCxr0Q)。

## Level.json

这是手动填写它的方式。手写比用编译器编写要好得多，因为**你不需要为它下载额外的软件**，更不用说**使用Cytoid谱面编译器的缺陷**（必须给它管理员权限）等等。在大多数情况下，手写的速度也要快得多，因此强烈推荐。请注意，“path”部分中的任何名称不必与示例相同，但音频的“path”和图像必须为.mp3（对于音频，不建议使用.wav）和.jpg / .png（用于图像）。

使用此作为参考指南。由于情况有可能不同，让我回答您下面可能遇到的所有问题。

请根据实际情况替换两个"-"里面的内容,并删除"-":

```json
{  
"version": -谱面版本号_纯数字-,
  "schema_version": 2,

  "id": "-你的cytoid账号-.-谱面名字-",
  
  "title": "-音乐标题-",
  "title_localized": "-音乐英文名-",

  "artist": "-曲师-",
  "artist_localized": "--曲师英文名-",
  "artist_source": "-曲师的链接-",

  "illustrator": "-画师-",
  "illustrator_source": "-画师的链接-",

  "charter": "-你的名字-",
  
  "music": {
    "path": "-音乐名称_.MP3_确保名称和音乐文件一致-"
  },
  "music_preview": {
    "path": "-预览音乐名称_.MP3_同上-"
  },
  "background": {
    "path": "-封面名称_.png or .jpg_同上-"
  },
  "charts": [
    {
      "type": "easy",
      "name": "-自定义难度名称，不需要则不填-"
      "difficulty": -难度等级_纯数字-,
      "path": "-谱面位置-"
    },
    {
      "type": "hard",
   "name": "-自定义难度名称-"
      "difficulty": -难度等级_纯数字-,
      "path": "-谱面位置-"
    },
    {
      "name": "-自定义难度名称-"
      "difficulty": -难度等级_纯数字-,
      "path": "-谱面位置-"
    }
  ]
  
}
```

## 常问问题：

### 问：我不需要3个难度。

A.删除不需要的难度，但请确保删除结尾逗号。例如，假设您只需要hard难度：

```
  "charts": [
    {
      "type": "easy",
    "name": "Lunatic"
      "difficulty": 9,
      "path": "lunatic.chart"
    },
    {
      "type": "hard",
   "name": "Very Hard"
      "difficulty": 10,
      "path": "hard.chart"
    },
    {
      "type": "extreme",
   "name": "Extreme Overload"
      "difficulty": 12,
      "path": "extreme.chart"
    }
  ]
```

在这里，你可以删除这样的部分。如果要删除extreme难度，请务必删除结束逗号！

```
  "charts": [
    {
      "type": "hard",
   "name": "Very Hard"
      "difficulty": 10,
      "path": "hard.chart"
    }
  ]
```



### 问：如何添加故事板？

答：如果每个难度没有超过2个不同的故事板，则无需将其包含在json中。但是，如果你有第3个故事板，那么

```
    {
      "type": "extreme",
      "name": "Extreme Overload",
      "difficulty": 15,
      "path": "extreme.chart",
      },
      "storyboard": {
       "path": "storyboard3.json"
      }
```

可以为不同谱面添加不同的故事板。storyboard.json的名称不一定是“storyboard3.json”。

### 问：我想为每个级别使用不同的音频文件，我该怎么办？

A.你可以像这样使用music_override：

```
    {
      "type": "extreme",
      "name": "Extreme Overload",
      "difficulty": 15,
      "path": "extreme.chart",
      "music_override": {
        "path": "music1.mp3"
      },
      "storyboard": {
       "path": "storyboard3.json"
      }
    }
```

添加music_override部分，并将要播放的音乐的“path”放在上面。

### 问：这太令人困惑了！给我一个关于level.json的完整示例。

好的，一个完整的level.json看起来像这样：

```
{
  
  "version": 2,
  "schema_version": 2,

  "id": "wz.yatm",
  
  "title": "You Are the Miserable",
  "title_localized": "",

  "artist": "t+pazolite, Laur",
  "artist_localized": "",
  "artist_source": "http://mutra.c-h-s.me/",

  "illustrator": "白祈QSR",
  "illustrator_source": "https://www.pixiv.net/member_illust.php?mode=medium&illust_id=69136806",

  "charter": "Wanderer Zariq",
  
  "music": {
    "path": "gc.mp3"
  },
  "music_preview": {
    "path": "preview.mp3"
  },
  "background": {
    "path": "background.jpg"
  },
  "charts": [
    {
      "type": "easy",
      "name": "GC",
      "difficulty": 13,
      "path": "chart.gc.txt",
      "storyboard": {
        "path": "storyboardgc.json"
      }
    },
    {
      "type": "hard",
      "name": "Uncut",
      "difficulty": 14,
      "path": "chart.uncut.txt",
      "music_override": {
       "path": "uncut.mp3"
      },
      "storyboard": {
       "path": "storyboarduncut.json"
      }
    },
    {
      "type": "extreme",
      "name": "Laur",
      "difficulty": 15,
      "path": "chart.laur.txt",
      "music_override": {
       "path": "laur.mp3"
      },
      "storyboard": {
       "path": "storyboardlaur.json"
      }
    }
  ]
  
}
```

以上为Wanderer Zariq的“You Are the Miserable”的例子。

## 使用编译器：[CLC Light](https://drive.google.com/file/d/1xDuM0wJJk26oVdh8v_NkkvXpnWylN9Ai/view?usp=sharing)

制作level的另一种方法是使用编译器编译它.

使用CLC Light本身很简单。

单击左上角的“导入<难度>”按钮选择谱面文件以导入谱面！导入后程序将自动输入地址。它还会检测您是否导入了图表的难度。这个过程是半自动的。确保填写所有详细信息，并在桌面上创建一个文件夹。

指定谱面Level ID后，请不要忘记验证谱面Level ID是否被占用，并确人是否添加背景图像。

> 译者:建议手动编写json,因为编译器会导致奇奇怪怪的问题
