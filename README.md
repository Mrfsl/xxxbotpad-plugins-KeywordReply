# xxxbotpad项目的 KeywordReply 关键词触发回复插件

## 使用
将这个项目的`KeywordReply`文件夹添加到xxxbot-pad项目中plugins目录即可

## 功能
关键词自动回复插件，根据配置的关键词自动回复消息
- 文本回复，直接回复配置文件`config.toml`中设置的信息
- 网页截图回复，可以发送指定网页的截图，以图片形式发送回复

## 截图服务
- 调用网络中截图api，插件中以`apiflash`为例，注意查看`main.py`中的`capture_webpage`函数
- 自己搭建，我的截图服务地址：`https://github.com/Mrfsl/puppeteer-screenshot-api/tree/main`


## 配置说明

编辑 `config.toml` 文件：

1. 在 `[basic]` 部分设置插件启用状态和优先级
2. 在 `[keywords]` 部分添加关键词回复配置，格式为：`"关键词" = "回复内容"`，截图回复形式“回复内容”为目标网页的url

## 示例

```toml
[keywords]
# 普通文本回复
"帮助" = "不帮不帮~"
"咕咕咕" = "朱颈斑鸠永远是我最好吃的朋友！!"
"查询" = "关键词包括：日程、打工日程、活动比赛、装备、祭典"

# 网页截图回复（需要截图的网页url）
"日程" = "https://splatoon3.ink"
"打工日程" = "https://splatoon3.ink/salmonrun"
"活动比赛" = "https://splatoon3.ink/challenges"
"装备" = "https://splatoon3.ink/gear"
"祭典" = "https://splatoon3.ink/splatfests"
```

## 打赏
<img src="https://github.com/user-attachments/assets/51a12660-2676-4f95-bee8-9999b08b13d1" style="width: 380px; height: auto; border: 1px solid #eee;" />

