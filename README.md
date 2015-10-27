#关于Android Studio集成资源混淆打包

这个Demo是通过集成微信早前开源的资源混淆工具到Android Studio里，在生成正式包时，自动化进行资源混淆，简化操作，提高效率。主要是在gradle脚本中添加一些代码，详见[app/build.gradle](app/build.gradle)

[微信团队开源的资源混淆工具](https://github.com/lendylongli/AndResGuard)

##其它注意事项
1、示例为了方便演示，将签名文件放到了`resources`目录下，而`local.properties`也是不应该加入版本控制的，这个需要注意。

2、相关资源混淆配置放在`resources/AndResGuard/config.xml`里，请加入相应的不需要混淆资源的配置(如通过反射方法获取的资源)，详细配置详见[点击这里](resources/AndResGuard/README.md)

3、为了保证资源混淆后的文件名统一性，建议将生成的`resource_mapping(`在`build/output/resguard`目录下)文件替换`resources/AndResGuard/resource_mapping.txt`

##关于作者
英文名:Leon

个人网站:[http://www.happycodeboy.com](http://www.happycodeboy.com)(想看更多相关Android的技术文章,[请点击](http://www.happycodeboy.com))

Email:codeboy2013@gmail.com
