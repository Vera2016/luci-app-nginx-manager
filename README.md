### 说明如下

1. 原项目地址：https://github.com/sundaqiang/openwrt-packages
2. 使用openwrt/luci编译原项目会缺少tabmenu.htm，运行会报错，对此问题进行了修改。（使用lede项目的luci好像没有问题）
3. 汉化不显示问题也修改了下

---------------------------------------下面是原项目README.md------------------------------------
# luci-app-nginx-manager（Nginx管理器）

更方便的管理openwrt的nginx

### 注意事项
1. 替代默认的uhttpd做为路由后台的web服务器
2. 插件依赖+luci-nginx +luci-ssl-nginx +luci-ssl-openssl，并且会开启路由后台的https功能
3. 插件会替代默认的uhttpd，但并不会删除uhttpd，如果你需要删除uhttpd，需在编译前在根目录执行以下操作：

```bash
sed -i 's/+uhttpd +uhttpd-mod-ubus //g' feeds/luci/collections/luci/Makefile
```

### 效果展示
![nginx-manager][1]

  [1]: https://raw.githubusercontent.com/sundaqiang/openwrt-packages/master/img/nginx-manager.png
