# BimiumAPI

* ## [ECIDI-API](#1)

  * [OpenTileSetViewer](#1-1)

  * [ChangeTileSet](#1-2)

  * [RefreshTileSetViewer](#1-3)

  * [DoSelection](#1-4)

  * [DoClearSelectionSet](#1-5)

  * [GetElementIdFromSelectionSet](#1-6)

  * [DoIsolateSelectionSet](#1-7)

  * [DoHideSelectionSet](#1-8)

  * [DoIsolateElement](#1-9)

  * [DoAddIsolateElement](#1-10)

  * [DoCancelIsolate](#1-11)

  * [DoHideElement](#1-12)

  * [DoCancelHide](#1-13)

  * [DoCancelDisplay](#1-14)

  * [DoRecoverCatagoryStatus](#1-15)

  * [DoSetElementColor](#1-16)

  * [DoCancelElementColor](#1-17)

  * [DoZoomIn](#1-18)

  * [DoZoomOut](#1-19)

  * [DoFitView](#1-20)

  * [DoWindowArea](#1-21)

  * [DoRotate](#1-22)

  * [DoPan](#1-23)

  * [DoWalk](#1-24)

  * [DoUndoView](#1-25)

  * [DoRedoView](#1-26)

  * [DoMeasureDistance](#1-27)

  * [DoMeasurePosition](#1-28)

  * [DoMeasureArea](#1-29)

  * [DoTransparencyToggle](#1-30)

  * [DoViewRotation](#1-31)

  * [DoShadowToggle](#1-32)

  * [DoCameraToggle](#1-33)

  * [DoGlobeToggle](#1-34)

  * [DoFullScreen](#1-35)

  * [DoZoomToElement](#1-36)

  * [ActivateViewByViewName](#1-37)

  * [DoSaveView](#1-38)

  * [DoChangeViewState](#1-39)



## ECIDI-API<h3 id="1"></h3>

<h3 id="1-1" ></h3>

### **ECIDI.OpenTileSetViewer**
---
### **描述：**

>加载模型

### **语法：**

    ECIDI.OpenTileSetViewer(viewJsonUrlArray, dependencies)

### **参数：**      

Name | Type | 	Description
---- | ---- |   -----------
viewJsonUrlArray | Array | 模型路径
dependencies | Object | 依赖项（可空）

### **返回值：**

>Promise对象

### **例子：**

    var viewJsonUrlArray = [
                    'http://bimsx.ecidi.com:6580/media/documents/meta/TileSets/shuxing/shuxing_AppData.json'
                       ];
    var dependencies = {
        labelText: "M",
        log: function() { console.log('label added'); },
        referencing: {
            isGeoreferenced : false
        }
    };

    ECIDI.OpenTileSetViewer(viewJsonUrlArray,dependencies).then(function(){
          ECIDI.DoSelection(true);
    });  
  
<br>



<h3 id="1-2" ></h3>

### **ECIDI.ChangeTileSet**
---
### **描述：**

>切换模型

### **语法：**

    ECIDI.ChangeTileSet(tilesetUrl)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
tilesetUrl | String | 模型路径

### **返回值：**

>Promise对象

### **例子：**
    function ChangeModel(path){
      ECIDI.ChangeTileSet(path).then(function(){
          ECIDI.DoSelection(true);
      });
    }
    ChangeModel('TileSets/JGDZ/JGDZ_AppData.json')

<br>



<h3 id="1-3" ></h3>

### **ECIDI.RefreshTileSetViewer**
---
### **描述：**

>重新加载模型视图框架

### **语法：**

    ECIDI.RefreshTileSetViewer()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-4" ></h3>

### **ECIDI.DoSelection**
---
### **描述：**

>启动选择工具

### **语法：**

    ECIDI.DoSelection(isActive)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
isActive | Boolean | 是否激活该工具


### **返回值：**

>无

### **例子：**

    ECIDI.DoSelection(true);

<br>

<h3 id="1-5" ></h3>

### **ECIDI.DoClearSelectionSet**
---
### **描述：**

>清除选择集

### **语法：**

    ECIDI.DoClearSelectionSet(isActive)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
isActive | Boolean | 是否激活该工具

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-6" ></h3>

### **ECIDI.GetElementIdFromSelectionSet**
---
### **描述：**

>获取选择集ID

### **语法：**

    ECIDI.GetElementIdFromSelectionSet()

### **参数：**

>无

### **返回值：**

Type | Description
---- | ----
Array | 元素ID集

### **例子：**

>无

<br>

<h3 id="1-7" ></h3>

### **ECIDI.DoIsolateSelectionSet**
---
### **描述：**

>选择集单独显示

### **语法：**

     ECIDI.DoIsolateSelectionSet(isActive)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
isActive | Boolean | 是否激活该工具

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-8" ></h3>

### **ECIDI.DoHideSelectionSet**
---
### **描述：**

>选择集隐藏

### **语法：**

     ECIDI.DoHideSelectionSet(isActive)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
isActive | Boolean | 是否激活该工具

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-9" ></h3>

### **ECIDI.DoIsolateElement**
---
### **描述：**

>元素对象隔离显示

### **语法：**

     ECIDI.DoIsolateElement(elementId)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
elementId | String/Array | 元素id

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-10" ></h3>

### **ECIDI.DoAddIsolateElement**
---
### **描述：**

>元素对象增量隔离显示

### **语法：**

     ECIDI.DoAddIsolateElement(elementId)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
elementId | String/Array | 元素id

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-11" ></h3>

### **ECIDI.DoCancelIsolate**
---
### **描述：**

>取消隔离显示效果

### **语法：**

     ECIDI.DoCancelIsolate()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-12" ></h3>

### **ECIDI.DoHideElement**
---
### **描述：**

>元素对象隐藏

### **语法：**

     ECIDI.DoHideElement(elementId)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
elementId | String/Array | 元素id

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-13" ></h3>

### **ECIDI.DoCancelHide**
---
### **描述：**

>取消隐藏效果

### **语法：**

     ECIDI.DoCancelHide()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-14" ></h3>

### **ECIDI.DoCancelDisplay**
---
### **描述：**

>取消隔离显示和隐藏效果，恢复显示状态

### **语法：**

     ECIDI.DoCancelDisplay()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-15" ></h3>

### **ECIDI.DoRecoverCatagoryStatus**
---
### **描述：**

>回复类型状态

### **语法：**

     ECIDI.DoRecoverCatagoryStatus()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-16" ></h3>

### **ECIDI.DoSetElementColor**
---
### **描述：**

>设置元素颜色及透明度

### **语法：**

     ECIDI.DoSetElementColor(elementId, color, alpha)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
elementId | String/Array | 元素id
color | Constant | 元素颜色 例：Cesium.Color.RED
alpha | Number | 透明度 0.0~1.0

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-17" ></h3>

### **ECIDI.DoCancelElementColor**
---
### **描述：**

>取消自定义元素颜色和透明度

### **语法：**

     ECIDI.DoCancelElementColor()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-18" ></h3>

### **ECIDI.DoZoomIn**
---
### **描述：**

>激活放大工具

### **语法：**

     ECIDI.DoZoomIn()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-19" ></h3>

### **ECIDI.DoZoomOut**
---
### **描述：**

>激活缩小工具

### **语法：**

     ECIDI.DoZoomOut()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-20" ></h3>

### **ECIDI.DoFitView**
---
### **描述：**

>视图全屏

### **语法：**

     ECIDI.DoFitView()

### **参数：**

>无

### **返回值：**

>无

### **例子：**

>无

<br>

<h3 id="1-21" ></h3>

### **ECIDI.DoWindowArea**
---
### **描述：**

>窗口放大 

### **语法：**

     ECIDI.DoWindowArea(isActive)

### **参数：**

Name | Type | 	Description
---- | ---- |   -----------
isActive | Boolean | 是否激活该工具

### **返回值：**

>无

### **例子：**

>无

<br>

