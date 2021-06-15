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
