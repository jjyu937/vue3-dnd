浏览器 API 无法在拖动开始后更改拖动预览或其行为。像 jQuery UI 这样的库实现了从头开始的拖放来解决这个问题，但是 react-dnd 目前只支持浏览器拖放“后端”，所以我们不得不接受它的局限性。但是，如果我们向浏览器提供一个空图像作为拖动预览，我们可以大量自定义行为。这个库提供了一个 DragLayer你可以用来在你的应用顶部实现一个固定的层，你可以在其中绘制一个自定义的拖动预览组件。请注意，如果我们愿意，我们可以在拖动层上绘制完全不同的组件。这不仅仅是一个屏幕截图。

使用这种方法，我们在离开容器时错过了默认的“返回”动画。但是，我们在自定义拖动反馈和零闪烁方面获得了极大的灵活性。

----
<br>
<br>
<br>

<script setup>
import CustomDragLayer from '../../.vitepress/examples/02-drag-around/custom-drag-layer'
</script>

<CustomDragLayer></CustomDragLayer>

[查看源码](https://github.com/hcg1023/vue3-dnd/tree/main/packages/docs/src/.vitepress/examples/02-drag-around/custom-drag-layer)