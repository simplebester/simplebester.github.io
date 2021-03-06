# cocos2d－x手册
这是一个cocos2d－x的学习纪录，主要思路是通过整个架构入手，熟练使用每一个api。最终形成一个参考手册。
整个游戏主要包含如下几类对象，无外乎排列组合而已。

## 坐标系
屏幕坐标系（UIKit）左上为原点。OpenGL坐标系左下为原点。
绝对，相对坐标系，锚点，对一个对象相对父节点的位置。

## CCDirector
### 工具
* convertToGL
* convertToUI

### 基本
* shareDirector
* get/setAnimationInterval
* is/setDisplayStats
* getSecondes
* set/getOpenGLView
* getTotalFrames

### 控制
* end
* is/pause
* resume
* start/stopAnimation
* getTouchDispatcher.addTargetedDelegate

### 窗口
* getWinSize
* getWinSizeInPixels
* getVisibleSize
* getVisibleOrigin

### 场景
* runWithScene
* getRunningScene
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

### 行为
* set/getActionManager
* run/stop/getAction
* set/get/is/Scheduler
* schedule/unschedule/Once/Update
* pause/resume/SchedulerAndAction

## CCRenderTexture
继承于CCNode
* begin
* end
* saveToFile

## CCScene
继承CCNode，大小等于窗口大小
* visit

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

## CCLayerMultiplex
一般用于选项卡，构造函数输入多个layer，用如下方法进行切换switchTo。

## CCRect
* CCRectMake
* containsPoint

## CCPoint
* ccpAdd
* ccpSub

## CCTouch
* getPreviousLocationsView

## TableView
一般用于构造关卡滚动界面，需要实现如下几个接口。create(parer,size),setDirection,setDelegate,reloadData,dequeueCell
### CCTableViewDataSource
* tableCellTouched
* tableCellSizeForIndex
* tableCellAtIndex
* numberOfCellsInTableView

### CCScrollViewDelegate

## CCSprit
继承于CCNodeRGBA，CCTextureProtocol，本质上就是一个二维图片。
### 基本
* init/withTexture/SpriteFrame/File
* set/getTexture/Rect
* set/getSpriteFrame
* set/getBlendFunc
* runAction

## SpriteFrame
* createWithTexture

## SpriteFrameCache
精灵缓冲，addSpriteFramesWithFile,spriteFrameByName

## CCTextureCache
## Texture2D

## CCSpriteBatchNode
* batchNodeWithTexture
* createWithTexture

## CCLabelTTF
静态文本create("")

## CCDictionary
读取配置文件，例如国际化，
* createWithContentsOfFile
* CCString转换char＊
* objectForKey

## CCArray
* createWithCapacity
* addObject

## CCAction
继承于CCObject
### 基本
* startWithTarget
* get/get/OriginalTaget
* isDone
### CCFolow
### CCSpeed
### CCActionInstant/Interval
### CCMoveTo
### CCAniMation
createWithSpriteFrames(frameArray),setLoop,setRestoreOriginalFrame

## CCMenu
CCMenu继承于CCLayer，因此具有触摸效果，CCMenuItem继承于CCNode没有触摸效果。
### CCMenu
    构造函数输入菜单条目，
* alignItem/Vertically/Horizontally/InRows/WithPadding
###     CCMenuItem
* CCMenuItemFont
* CCMenuItemImage
- setNormal/Selected/SpriteFrame
    构造函数输入noraml、select态的图片，回调函数（menu_selector）
* CCMenuItemToggle

## SimpleAudioEngine
* preloadBackgroundMusic
* preloadEffect
* play/stop/BackgroundMusic
* palyEffect

## CCScale9Sprite

## CCControlButton
* setBackgroundSpriteForState
* setPreferredSize
* addTargetWithActionForControlEvents


