[TOC]

## Mybatis3-yanxi 学习笔记

**[mybatis3官方文档](<https://blog.mybatis.org/>)**

#### 1、Configuration



```
| logImpl
	-| 日志实现
| vfsImpl
	-| 虚拟文件系统，默认实现：JBoss6VFS、DefaultVFS
| LocalCacheScop
	-| SESSION(default),STATEMENT
| ExecutorType
	-| SIMPLE(default)
	-| REUSE 执行器重用 
  -| BATCH 执行器重用语句，批量更新
| AutoMappingBehavior ， 自动映射行为
	-| NONE: Disables auto-mapping.
	-| PARTIAL(default): Will only auto-map results with no nested result mappings defined inside.
	-| FULL: Will auto-map result mappings of any complexity (containing nested or otherwise).
| AutoMappingUnknownColumnBehavior , 匹配到未知的列如何处理
	-| NONE(default): Do Nothing 
	-| WARNING: Output warning log.
	-| FAILING: Fail mapping.
| ReflectorFactory , 反射工厂类
| ObjectFactory ， 对象工厂类，实例化对象
| objectWrapperFactory
---------
· 对象导航图语言（Object Graph Navigation Language），简称OGNL
---------
| ProxyFactory (JavassistProxyFactory)
---------
| MapperRegistry ： interface mapper映射
| InterceptorChain ： mybatis拦截器 
| TypeHandlerRegistry ： 类型处理handler
| TypeAliasRegistry ： 类型别名映射
| LanguageDriverRegistry ： 注解配置SQL更灵活
	-| XMLLanguageDriver(default)
--------- ？？？待看↓
| mappedStatements
| caches
| resultMaps
| parameterMaps
| keyGenerators
---------
| loadedResources
| sqlFragments
---------
| Collection<XMLStatementBuilder> incompleteStatements
| Collection<CacheRefResolver> incompleteCacheRefs
| Collection<ResultMapResolver> incompleteResultMaps
| Collection<MethodResolver> incompleteMethods
| Map<String, String> cacheRefMap
	

```







