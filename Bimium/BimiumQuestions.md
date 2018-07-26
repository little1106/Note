## BimiumQuestions



1. 双屏模式我尝试新建viewer时，提示  while creating TileSetViewer dependencies Error: Component bim-list is already registered.

2. 此 ComponentFactory.registerComponents(); 注册的意义是啥？

```javascript
registerComponents: function registerComponents() {
            //Cesium.knockout.bindingHandlers['css2'] = Cesium.knockout.bindingHandlers.css;
            for (var id in ComponentId) {
                var component = ComponentFactory.getComponentDefinition(ComponentId[id]);
                Cesium.knockout.components.register(ComponentId[id], {
                    viewModel: component.viewModel,
                    template: component.template
                });
            }
        }
```




