## 帮助文档

### 简介

小点阅读器是一款可以自定义规则来获得极佳阅读体验的app，用户只要掌握一点html和css技巧，就能自定义规则，截取网页的内容。

### 使用帮助

#### 订阅页面，这里只能添加dotreader后缀的纯文本链接。

```
正确的链接  https://raw.githubusercontent.com/m3u8playlist/reader/main/source/gold-miner.dotreader
错误的链接  https://github.com/m3u8playlist/reader/blob/main/source/gold-miner.dotreader
```
第一个是纯文本，可以添加到订阅，第二个是网页，不可添加到订阅

订阅页面右上角的3个图标从左往右依次是：
1. 更新全部规则
2. 排序
3. 添加订阅


#### RSS页面，这里可以添加网页的rss链接

RSS页面右上角的2个图标从左往右依次是：
1. 排序
2. 添加订阅


### 订阅文件

订阅文件是以.dotreader结尾的文本文件，只要添加数行css select规则即可。

以下是一个实例文件

```
sub_title=掘金翻译计划
sub_type=txt
sub_flag=true
sub_is_image_only_flag=false
sub_has_multiple_pages_flag=false
sub_can_search_flag=false
sub_tags=iOS,区块链,人工智能,Android,前端,后端,设计,产品,其他
sub_first_url=https://github.com/xitu/gold-miner/blob/master/ios.md,https://github.com/xitu/gold-miner/blob/master/blockchain.md,https://github.com/xitu/gold-miner/blob/master/AI.md,https://github.com/xitu/gold-miner/blob/master/android.md,https://github.com/xitu/gold-miner/blob/master/front-end.md,https://github.com/xitu/gold-miner/blob/master/backend.md,https://github.com/xitu/gold-miner/blob/master/design.md,https://github.com/xitu/gold-miner/blob/master/product.md,https://github.com/xitu/gold-miner/blob/master/others.md
sub_other_url_pre=none,none,none,none,none,none,none,none,none
sub_other_url_suffix=none
sub_rule_container_select=#repo-content-pjax-container #readme ul
sub_rule_items_select=li
sub_rule_date_select=none
sub_rule_title_select=a
sub_rule_title_select_attr=none
sub_rule_logo_select=none
sub_rule_logo_select_attr=none
sub_rule_url_select=a
sub_rule_url_select_attr=href
sub_rule_logo_pre=none
sub_rule_url_pre=none
item_rule_container_select=.container .markdown-body
item_rule_img_replace_flag=false
item_rule_img_replace_s=none
item_rule_img_replace_t=none
item_rule_img_select=none
item_rule_img_select_attr=none
sub_second_container_select=none
sub_second_items_select=none
sub_second_title_select=none
sub_second_title_select_attr=none
sub_second_url_select=none
sub_second_url_select_attr=none
sub_second_url_pre=none
sub_search_url=none
sub_search_url2=none
sub_search_first_container_select=none
sub_search_first_items_select=none
sub_search_title_select=none
sub_search_title_select_attr=none
sub_search_logo_select=none
sub_search_logo_select_attr=none
sub_search_first_url_select=none
sub_search_first_url_select_attr=none
sub_search_logo_pre=none
sub_search_first_url_pre=none
```

=号前面不可更改，=号后面是用户自定义的规则




#### 条目解释

```
sub_title=掘金翻译计划
```
添加订阅后显示在首页的名字，可以任取



```
sub_type=txt
```
这是订阅的显示类型，分为三种
+ txt
+ landscape
+ portrait

txt的主题列表是不显示图标的
landscape的主题列表显示横向的图片
portrait的主题列表显示纵向的图片

```
sub_flag
```
一般网站设置成true

```
sub_is_image_only_flag=false
```
文章是否是纯图片内容，如果是纯图片则设置true，否则设置false


```
sub_has_multiple_pages_flag=false
```
是否带有章节，如果带有章节，则设置true，如果不带章节，文章列表点击直接进入文章，则显示false。如果设置为true，需填写sub_second系列的解析规则，否则全部填none

```
sub_can_search_flag=false
```
是否可以搜索，如果可以，则设置true，否则设置false。如果设置为true，需填写sub_search系列的解析规则，否则全部填none

```
sub_tags=iOS,区块链,人工智能,Android,前端,后端,设计,产品,其他
```
这是分类，一个网站可以有不同的分类，在这里设置所有的分类，中间用英文逗号连接



```
sub_first_url=https://github.com/xitu/gold-miner/blob/master/ios.md,https://github.com/xitu/gold-miner/blob/master/blockchain.md,https://github.com/xitu/gold-miner/blob/master/AI.md,https://github.com/xitu/gold-miner/blob/master/android.md,https://github.com/xitu/gold-miner/blob/master/front-end.md,https://github.com/xitu/gold-miner/blob/master/backend.md,https://github.com/xitu/gold-miner/blob/master/design.md,https://github.com/xitu/gold-miner/blob/master/product.md,https://github.com/xitu/gold-miner/blob/master/others.md
```
这是每个分类第一页对应的网址，中间用英文逗号连接，数目必须和上面的sub_tags数目一致



```
sub_other_url_pre=none,none,none,none,none,none,none,none,none
```
这是每个分类后续页面对应的网址前半部分（即页数的前部分），中间用英文逗号连接，数目必须和上面的sub_tags数目一致




```
sub_other_url_suffix=none
```
这是每个分类后续页面对应的网址后半部分（即页数的后部分），中间用英文逗号连接，数目必须和上面的sub_tags数目一致，如没有则填none



```
sub_rule_container_select=#repo-content-pjax-container #readme ul
```
这是要截图的主题列表总的容器



```
sub_rule_items_select=li
```
这是要截图的主题列表每个主题的容器



```
sub_rule_date_select=none
```
这是选择每个主题日期的容器，如没有则填none


```
sub_rule_title_select=a
```
这是选择每个主题标题的容器

```
sub_rule_title_select_attr=none
```
这是选择每个主题标题容器的属性，如没有则填none。 比如```<h4>foo bar</h4>```, 则填none，比如```<span alt="foo bar">other string</span>```,则填 alt


```
sub_rule_logo_select=none
```
这是选择每个主题图标的容器，如果sub_has_logo=false，则填none

```
sub_rule_logo_select_attr=none
```
这是选择每个主题图标容器的属性，如没有则填none。 比如```<h4>foo bar</h4>```, 则填none，比如```<span alt="foo bar">other string</span>```,则填 alt，如果sub_has_logo=false，则填none


```
sub_rule_url_select=a
```
这是选择每个主题链接的容器

```
sub_rule_url_select_attr=href
```
这是选择每个主题标题链接的属性，如没有则填none。 比如```<p>http://example.com</p>```, 则填none，比如```<a href="http://example.com">link</a>```,则填 href


```
sub_rule_logo_pre=none
```
如果图片是相对链接，则补全网站域名，否则填none

```
sub_rule_url_pre=none
```
如果链接是相对链接，则补全网站域名，否则填none

```
item_rule_container_select=.container .markdown-body
```
这是单个主题页面的内容的容器




```
item_rule_img_replace_flag=false
```
选择是否替换图片链接，如要替换填true，否则填false。 此规则仅在sub_is_image_only_flag=false时有效

```
item_rule_img_replace_s=none
```
选择要替换的内容。此规则仅在sub_is_image_only_flag=false时有效


```
item_rule_img_replace_t=none
```
替换后的内容。此规则仅在sub_is_image_only_flag=false时有效



```
item_rule_img_select=none
```
选择图片的容器，此规则仅在sub_is_image_only_flag=true时有效，否则填none


```
item_rule_img_select_attr=none
```
选择图片的容器的属性，此规则仅在sub_is_image_only_flag=true时有效，否则填none


#### 如果sub_has_multiple_pages_flag=true，即带有章节，需填写以下规则，否则全部填none

```
sub_second_container_select=none
```
章节页面的章节列表的总的容器



```
sub_second_items_select=none
```
每个章节的容器


```
sub_second_title_select=none
```
章节名字的容器


```
sub_second_title_select_attr=none
```
章节名字的容器的属性


```
sub_second_url_select=none
```
章节链接的容器


```
sub_second_url_select_attr=none
```
章节链接的容器的属性


```
sub_second_url_pre=none
```
如果章节是相对链接，则补全网站域名，否则填none




#### 如果sub_can_search_flag=true，即可以搜索文章，需填写以下规则，否则全部填none

```
sub_search_url=none
```

搜索页面的网址，比如https://www.example.com/search/?keyword=`
关键字位置用`取代


```
sub_search_url2=none
```
搜索页面的第二页开始的网址，比如https://www.example.com/search/?keyword=`&page=^
关键字位置用`取代，页数用^取代


```
sub_search_first_container_select=none
```
搜索页文章列表的容器

```
sub_search_first_items_select=none
```
搜索页每篇文章的容器

```
sub_search_title_select=none
```
搜索页每篇文章标题的容器

```
sub_search_title_select_attr=none
```
搜索页每篇文章标题的容器的属性

```
sub_search_logo_select=none
```
搜索页每篇文章图片的容器

```
sub_search_logo_select_attr=none
```
搜索页每篇文章图片的容器的属性

```
sub_search_first_url_select=none
```
搜索页每篇文章链接的容器

```
sub_search_first_url_select_attr=none
```
搜索页每篇文章链接的容器的属性

```
sub_search_logo_pre=none
```
如果图片是相对链接，则补全网站域名，否则填none

```
sub_search_first_url_pre=none
```
如果搜索页的文章是相对链接，则补全网站域名，否则填none



#### 补充说明

```
<img ess-data='https://www.yudaotu.com/images/2021/06/14/1G1n.jpg' />
```
如上所示，因为webview只能显示 img src=xxx，所以需要将ess-data替换成src

```
item_rule_img_replace_flag=true
item_rule_img_replace_s=ess-data
item_rule_img_replace_t=src
```


