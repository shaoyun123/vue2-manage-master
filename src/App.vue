<template>
    <div id="app" class="fillcontain">
		    <router-view></router-view>
    </div>
</template>

<script>
    export default {
    	created () {
    	  setTimeout(() => {   // 定时器，created执行一秒后触发
    	    window.L2Dwidget.init({
    	      pluginRootPath: 'static/live2dw/',    // 本地目录
    	      pluginJsPath: 'lib/',    // 本地目录
    	      pluginModelPath: 'live2d-widget-model-koharu/assets/',    // live2d-widget-model-   "koharu" 这个是换人物
    	      tagMode: false,
    	      debug: false,
    	      model: { jsonPath: '/static/live2dw/live2d-widget-model-koharu/assets/koharu.model.json' },
    	      display: { position: 'left', width: 150, height: 300 },  // 调整大小和位置
    	      mobile: { show: true },  // 是否盯着鼠标看
    	      log: false
    	    })
    	  }, 1000)
    	}
    }
</script>

<style lang="less">
	@import './style/common';
</style>
