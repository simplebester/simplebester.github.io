# cocos2d－x手册
这是一个cocos2d－x的学习纪录，主要思路是通过整个架构入手，熟练使用每一个api。最终形成一个参考手册。
整个游戏主要包含如下几类对象，无外乎排列组合而已。

## CCDirector
### 基本
* shareDirector
* getRunningScene
* get/setAnimationInterval
* is/setDisplayStats
* getSecondes
* set/getOpenGLView
* isPaused
* getTotalFrames

### 控制
* end
* is/pause
* resume
* start/stopAnimation

### 窗口
* getWinSize
* getWinSizeInPixels
* getVisibleSize
* getVisibleOrigin
* convertToGL
* convertToUI

### 场景
* runWithScene
* pushScene
* popScene
* popToRootScene
* popToSceneStackLevel
* replaceScene

## CCNode
### 基本
* get/setPosition/X/Y
* get/setScale/X/Y
* get/setZOrder
* get/setSkewX/Y
* get/setAnchorPoint/InPoints
* get/setConentSize
* set/isVisible
* get/setRotation/X/Y
* convertToNode/WorldSpace
* convertTouchToNodeSpace

### 数据
* get/setTag
* get/setUserData
* get/setUserObject

### 场景
* add/getChild/removeChild/removeAllChild
* set/get/removeFromParent
* reorderChild

### 回调
* onEnter/TansitionDidFinish
* onExit/TansitionDidFinish
* update

### 行为
* set/getActionManager
* run/stop/getAction
* set/get/is/Scheduler
* schedule/unschedule/Once/Update

## CCScene
继承CCNode，大小等于窗口大小
## CCLayer
继承CCNode，CCTouch，CCAccelerometer，CCKeyBoard
### 基本
* is/setToucheEnabled
* set/getTouchMode
* get/setTouchPriority
* is/set/getAccelerometerEnabled/Interval
* is/setKeypadEnabled

### 事件
* ccTouch/Touches/Began/Moved/Ended/Canceled
* registerWithTouchDispatcher
* didAccelerate/reg/unregScriptAccelerateHandler
* keyBack/Menu/Clicked

## CCSprit
继承于CCNodeRGBA，CCTextureProtocol，本质上就是一个二维图片。
### 基本
* init/withTexture/SpriteFrame/File
* set/getTexture/Rect
* set/getSpriteFrame
* set/getBlendFunc

## Texture2D

## CCAction
