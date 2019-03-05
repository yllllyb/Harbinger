## 原版铁砧相关

虽然原版铁砧实际上没有标准化的“配方”概念，但 Forge 仍然提供了相关事件，我们可以利用这些事件模拟出“铁砧配方”的效果。

### `AnvilUpdateEvent`

可取消，无结果，在玩家往铁砧的界面里放东西时会发布，通过这个事件可以修改最终的“修复”产物和“修复”材料消耗数量。取消事件后即可接管原版的铁砧修复逻辑，从而实现类似“铁砧配方”的效果。

### `AnvilRepairEvent`

不可取消，无结果，在玩家取出修复的产物时发布，主要用于决定铁砧是否会在此之后损坏。