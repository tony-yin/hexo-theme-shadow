# hexo-theme-shadow

## 关于主题

本主题是根据[balck-blue][1]主题扩展而成，所做扩展如下：

1. 添加左侧栏`segmentfault`小图标
2. 更新`requirejs`源为`https`，避免`https`网站引入`http`脚本时浏览器告警
3. 更新`jquery`源为`https`，避免`https`网站引入`http`脚本时浏览器告警
4. 更新`baidu`分享源到本地，避免`https`网站引入`http`脚本时浏览器告警
5. 更新`code word`的风格，具体参见博客
6. 更改了全局的代码词颜色样式
7. 原来项目编号中的代码样式是白色的，不是很好看，也进行了相应的更新
8. 将头像从懒加载改为了直接加载，懒加载头像需要很长时间，用户体验很差
9. 网站背景音乐添加支持
10. 代码块样式修改
11. 三级、四级和五级标题样式修改
12. 链接样式修改
13. 畅言打赏支持
14. 书签区域样式修改
15. 项目编号样式修改
16. `table`样式修改

## 使用

### 安装

```
git clone git@github.com:tony-yin/hexo-theme-shadow.git themes/shadow
```

### 配置

修改`hexo`根目录下的`_config.yml`： `theme: shadow`

### 更新

```
cd themes/shadow
git pull
```

### 配置

主题配置文件在主目录下的`_config.yml`，请根据自己需要修改使用。 部分可以参考我的配置：

```
# >>> Basic Setup | 基础设置 <<<

# Header | 主菜单
## About Page: `hexo new page about`
## Tags Cloud Page: `hexo new page tags`
menu:
  所有文章: /archives/
  技术文章: /categories/tech
  感悟总结: /categories/summary
  阅读翻译: /categories/read
  好文转载: /categories/reprinted
  生活随笔: /categories/life
  关于我: /about/

# Link to your avatar | 填写头像地址
avatar: /img/avatar.png

# Small icon of Your site | 站点小图标地址
favicon: /img/favicon.png

# Social info. Bar | 社交信息展示
## Keep "mailto:" in Email | 设置 Email 时保留 "mailto:"
## Encrypt email 加密邮件地址 http://ctrlq.org/encode/
## RSS requires a plugin to take effect | 使用 RSS 需先安装对应插件
## https://github.com/hexojs/hexo-generator-feed
subnav:
  github: xxxxx
  weibo: xxxxxxxx
  rss: /atom.xml

  # Google: "#"
# search_box: true

# >>> Conments 评论系统 <<<

disqus:
  on: false
  shortname: xxxxxxxxx
  # https://help.disqus.com/customer/en/portal/articles/466208-what-s-a-shortname-
  # It is unnecessary to enable disqus here if
  # you have set "disqus_shortname" in your site's "_config.yml"
changyan:
  on: false
  appid: xxxx
  conf: xxxxxxxxx
  # 是否开启畅言评论，
  # id 中填写你的友言用户数字ID，注册后进入后台管理即可查看
  # 畅言评论在 Web 环境下运行，普通本地环境无法查看，请部署后在线上测试。
reward:
  on: true
  # 是否开启打赏
  # 这里的打赏是基于畅言的，所以必须要开启畅言再开启这里的打赏才可以生效
  # 打赏还有一些设置需要去畅言后台设置
  
# >>> Style Customisation 样式自定义 <<<

# Background | 背景
## "background_sum": show images form /source/background/的图片数目
## "on: true": 自动随机显示这5张图片
## "on: false": 自定义显示图片设置background_image: 5
background:
  on: true
  background_sum: 4
  background_image: 4

highlight_style:
  on: true
  inline_code: 3  # Value: 0 - 9 可选
  code_block: 2  # Value: 0 - 4
  # Set inline_code to style highlight text
  # Chose a highlight theme for code block
  # 通过 inline_code 切换内置文本高亮样式
  # 通过 code_block 切换内置代码高亮配色主题

blockquote_style:
  #on: true
  blockquote: 5  # Value: 0 - 7 可选
  # 自定义文章「引用部分」的样式

# 左边栏宽度 px
left_col_width: 300

# 目录中标题不换行
# Keep TOC title on the same line |
toc_nowrap: false

# 自定义"阅读全文"链接按钮的显示文字
# Customize the text on excerpt link
excerpt_link: 阅读全文 #修改more>>的文字

# 是否显示边栏中的搜索框（站内搜索）
# Search Box in left column
search_box: true

# 是否开启主页及加载头像时的动画效果
# Animation in Homepage and Loading avatar
animate: true

# >>> Small features | 小功能设置 <<<

# 是否开启边栏多标签切换
# Birdhouse button in left column
tagcloud: true

# Blogroll, Link exchange | 友情链接
# friends: false
friends:
  xxx: http://www.baidu.com
#是否开启“关于我”。
aboutme: 江苏南京，熟悉Python/PHP，目前研究Ceph分布式存储，邮箱：1241484989@qq.com
#aboutme: false

# 是否在新窗口打开链接
open_in_new: false

# Customize feed link 自定义订阅地址
rss: /atom.xml


# >>> Vendors | 第三方工具 & 服务 <<<

# images viewer | 图片浏览器
## http://www.fancyapps.com/fancybox/
fancybox: true

# Display Math(LaTeX, MathML...) | 数学公式支持
## https://www.mathjax.org/
mathjax: false

# Socail Share | 是否开启分享
# share: true
baidushare: true
#showshare: true

# 百度、谷歌站长验证。填写 HTML 标签 content
# Site Verification for Google and Baidu. HTML label content.
# google_site: # pFW527fHrjfI0si2w4NQ0w3cTw12AvvuohAu1PUfqKA
# baidu_site: #c167b9feb4f0b208b712c79629c188e4

# Fill in Google Analytics tracking ID, #e.g. UA-XXXXX-X, or Baidu Analytics hash key
google_analytics: xxxxx
baidu_analytics: xxxxxx



# 不蒜子网站计数设置
# http://ibruce.info/2015/04/04/busuanzi/
visit_counter:
  on: true
  site_visit: 极客到访数
  page_visit: 本页阅读量


# A标签提示
TipTitle: true

# Loading
# Loading: true

# 背景音乐 
music:
  on: true
  url: //music.163.com/outchain/player?type=0&id=2021839040&auto=1&height=32
  # 可以通过网易云音乐获取外链，替换上面的链接即可

```

[1]: https://github.com/maochunguang/black-blue
