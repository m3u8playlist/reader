## 帮助文档

### 简介

小点阅读器是一款可以自定义规则来获得极佳阅读体验的app，用户只要掌握一点html和css技巧，就能自定义规则，截取网页的内容。

### 订阅文件

订阅文件是以.dotreader结尾的文本文件，只要添加数行css select规则即可。

以下是一个实例文件

```
sub_title=掘金翻译计划
sub_has_logo=false
sub_flag=true
sub_tags=iOS,区块链,人工智能,Android,前端,后端,设计,产品,其他
sub_first_url=https://github.com/xitu/gold-miner/blob/master/ios.md,https://github.com/xitu/gold-miner/blob/master/blockchain.md,https://github.com/xitu/gold-miner/blob/master/AI.md,https://github.com/xitu/gold-miner/blob/master/android.md,https://github.com/xitu/gold-miner/blob/master/front-end.md,https://github.com/xitu/gold-miner/blob/master/backend.md,https://github.com/xitu/gold-miner/blob/master/design.md,https://github.com/xitu/gold-miner/blob/master/product.md,https://github.com/xitu/gold-miner/blob/master/others.md
sub_more_url_pre=none,none,none,none,none,none,none,none,none
sub_more_url_suffix=none
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
```

=号前面不可更改，=号后面是用户自定义的规则
```
sub_title=掘金翻译计划
```
添加订阅后显示在首页的名字，可以任取


```
sub_has_logo=false
```
主题列表是否带图片，如果带图片则设置true，否则设置false


```
sub_flag=true
```
一般设置成true即可



```
sub_tags=iOS,区块链,人工智能,Android,前端,后端,设计,产品,其他
```
这是分类，一个网站可以有不同的分类，在这里设置所有的分类，中间用英文逗号连接



```
sub_first_url=https://github.com/xitu/gold-miner/blob/master/ios.md,https://github.com/xitu/gold-miner/blob/master/blockchain.md,https://github.com/xitu/gold-miner/blob/master/AI.md,https://github.com/xitu/gold-miner/blob/master/android.md,https://github.com/xitu/gold-miner/blob/master/front-end.md,https://github.com/xitu/gold-miner/blob/master/backend.md,https://github.com/xitu/gold-miner/blob/master/design.md,https://github.com/xitu/gold-miner/blob/master/product.md,https://github.com/xitu/gold-miner/blob/master/others.md
```
这是每个分类第一页对应的网址，中间用英文逗号连接，数目必须和上面的sub_tags数目一致



```
sub_more_url_pre=none,none,none,none,none,none,none,none,none
```
这是每个分类后续页面对应的网址前半部分（即页数的前部分），中间用英文逗号连接，数目必须和上面的sub_tags数目一致




```
sub_more_url_suffix=none
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
这是选择每个主题标题容器的属性，如没有则填none。 比如<h4>foo bar</h4>, 则填none，比如<span alt="foo bar">other string</span>,则填 alt


```
sub_rule_logo_select=none
```
这是选择每个主题图标的容器，如果sub_has_logo=false，则填none

```
sub_rule_logo_select_attr=none
```
这是选择每个主题图标容器的属性，如没有则填none。 比如<h4>foo bar</h4>, 则填none，比如<span alt="foo bar">other string</span>,则填 alt，如果sub_has_logo=false，则填none


```
sub_rule_url_select=a
```
这是选择每个主题链接的容器

```
sub_rule_url_select_attr=href
```
这是选择每个主题标题链接的属性，如没有则填none。 比如<p>http://example.com</p>, 则填none，比如<a href="http://example.com">link</a>,则填 href


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
选择是否替换图片链接，如要替换填true，否则填false

```
item_rule_img_replace_s=none
```
选择要替换的内容


```
item_rule_img_replace_t=none
```
替换后的内容


关于最后三条的补充说明

```
<img ess-data='https://www.yudaotu.com/images/2021/06/14/1G1n.jpg' />
```
如上所示，因为webview只能显示 img src=xxx，所以需要将ess-data替换成src

```
item_rule_img_replace_flag=true
item_rule_img_replace_s=ess-data
item_rule_img_replace_t=src
```









