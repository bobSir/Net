[net](../index.md) / [com.drake.net](index.md) / [syncDownload](./sync-download.md)

# syncDownload

`fun syncDownload(path: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, dir: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = NetConfig.app.externalCacheDir!!.absolutePath, tag: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`? = null, absolutePath: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, method: RequestMethod = RequestMethod.GET, uid: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`? = null, block: Api.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)` = {}): `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)

同步文件下载, 默认Get请求

### Parameters

`path` - String 请求路径, 非绝对路径会加上[NetConfig.host](-net-config/host.md)为前缀

`tag` - 可以传递对象给Request请求, 一般用于在拦截器/转换器中进行针对某个接口行为判断

`absolutePath` - 请求路径是否是绝对路径

`uid` - 表示请求的唯一id, 和[NetCancel.cancel](#)中的uid一致, 一般用于指定取消网络请求的唯一id

`block` - 函数中可以配置请求参数