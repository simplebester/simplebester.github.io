# Cocos2d-x
## 一、屏幕适配
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
