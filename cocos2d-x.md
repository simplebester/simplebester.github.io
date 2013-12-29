# Cocos2d-x
## 一、工程创建
使用cocos2d自带的创建工程的脚本进行工程创建：

    create_project.py -project MyGame -package com.MyCompany.AwesomeGame -language javascript

与cocosbuilder融合创建资源，只需目录上的一个tip，注意让两个Resource覆盖就行。
Create folder references for any added folders

## 二、屏幕适配
### 1、资源精度
#### 分类
* iphone
* ipad
* ipad retina
#### 方案
* setSearchPaths
* setSearchResolutionsOrder
### 2、长宽比
#### 分类
* 3:2
* 16:9
* 16:10
* iphone4s
* 其他
#### 方案
* setFrameSize frmaesize
* setDesignResolutionSize，winsize VisibleSize，
  1. kResolutionShowAll  四周留白
  2. kResolutionExactFit 拉伸到屏幕
  3. kResolutionNoBorder 撑出屏幕外
### 3、设计与运行大小差异
* setContentScaleFactor
## 
