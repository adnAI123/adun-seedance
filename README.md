# adun-seedance

AI 视频导演 Skill：先当导演把戏想透，再写成视频模型一条就能跑出来的提示词。

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Standard-green)](https://agentskills.io)
[![Models](https://img.shields.io/badge/Models-Seedance%202.5%20%C2%B7%20MAGI--2%20%C2%B7%20Kling%204.0%20%C2%B7%20Wan%203.0-orange)](#支持的模型)
[![Runtime](https://img.shields.io/badge/Runtime-Claude%20Code%20%C2%B7%20Codex%20%C2%B7%20%E8%B1%86%E5%8C%85%E5%B7%A5%E4%BD%9C%20%C2%B7%20Cursor-blueviolet)](#安装)

作者阿墩AI，《瑶瑶乱三界》《神坛之下》导演，全网播放破亿，抖音 35.8 万粉。成片见抖音 [@阿墩的AI小剧场](https://www.douyin.com/user/MS4wLjABAAAAn_KY49e4Ffpz1a7jHSerUUn2MBpjzcTPk0UsbkRHuJBeUA1W8hxE8tpNoauGFygg)。

## 安装

```bash
npx skills add adnAI123/adun-seedance -g
```

Claude Code、Codex、Cursor、Gemini CLI、Trae 等都认这条，需要 Node.js 22.20 以上。也可以把这条命令直接发给豆包工作这类 AI，让它替你跑。

Claude Code 插件：

```
/plugin marketplace add adnAI123/adun-seedance
/plugin install adun-seedance@adun-seedance
```

或者把链接丢给你的 AI：

```
安装这个 skill：https://github.com/adnAI123/adun-seedance
```

都不行的，到 [Releases](https://github.com/adnAI123/adun-seedance/releases/latest) 下载压缩包，在 AI 的技能页面上传。

## 怎么用

### 从剧本到提示词

1. 把剧本和参考图（人物图、场景图）发给 AI，说「设计这一段」。
2. 方向没定，它先给三版构想：三位导演三种拍法，每版从起拍讲到收尾，标出首选和理由。你挑一版，或者说要哪版的哪一部分。
3. 选定后它深化成导演设计：这段多长、从哪接、停在哪，人怎么演、镜头怎么走、每一招从哪来打到哪、声音怎么配。你提意见，它改，到你满意为止。
4. 说「写提示词」。它按定稿落笔，每条把站位、朝向、兵器、机位、光、声音写全，写完自查一遍再交。
5. 提示词贴进视频模型，挂上参考图生成。

### 成片不对

把成片发回去，它按实际秒数逐段对照设计，指出是哪一句没写准，改那一句。局部问题它会先建议剪裁或用平台的视频编辑修，要整条重跑由你定。

### 其他用法

- 分镜已经想好：直接说只要提示词，跳过设计。
- 连续剧：说「下一段」，它接着上一段结尾的站位、动势和人物心境往下设计。
- 系列项目：成片满意了说「存档」，它按 `templates/PROJECT.md` 建项目档案，记下人物、资产和已拍段落，后面每集接着用。
- 换模型：告诉它这个模型单条最长几秒、参考图怎么引用，它照这个写。
- 走位特别复杂的多人长镜头，可以让它搭 3D 白模锁住站位和运镜，见 `core/baimo.md`。

## 支持的模型

支持全能参考的视频模型都能用：Seedance 2.5、Seedance 2.5 Flash、Seedance 2.0、MAGI-2、Kling 4.0、Wan 3.0。附带的 77 篇案例和平台手册出自即梦上的 Seedance 2.0 与 2.5。

## 仓库里有什么

```
skills/adun-seedance-v3/
├── SKILL.md         导演：想戏、三版构想、导演设计
├── core/
│   ├── format.md    落笔：提示词格式、写完自查
│   ├── platform.md  即梦平台手册：参数、审核、@ 引用、延长和编辑
│   ├── 维护.md      成片复查、补拍、项目存档
│   └── baimo.md     3D 白模锁走位
├── cases/           77 篇实拍提示词，按戏的类型建了索引
└── templates/       项目档案模板
```

## 许可

© 2026 阿墩AI，[CC BY-NC-SA 4.0](LICENSE)：转载署名并附链接，不得商用，改编按同协议开放。商用授权私信 X [@adnAI123](https://x.com/adnAI123)。欢迎投稿实测案例，见 [CONTRIBUTING.md](CONTRIBUTING.md)。
