# CHANGES 2018-4-30
- chrome 63

## 整个框架的重新优化
-   Base层管理常用方法
-   PageObject层管处理页面逻辑
-  TestCase 测试用例调用，调用Page层，传入yaml用例
-  yaml测试用例编写层，基于关键字驱动，主要包含
    - testinfo. 用例介绍
    - testcase. 用例操作步骤，用例操作步骤
    - check. 检查点
-  Runner入口
-  Log记录每台设备多运行日志，含截图
- Report 自动生成excel测试报告

## 其他优化
- setupclass+ self.driver.get重定位的方式，避免用例依赖和每个用例重连session
- 常用的异常封装，不会因为一些异常造成框架无法运行
- 检查点的支持，支持：
    - CONTRARY = "contrary" # 相反检查点，表示如果检查元素存在就说明失败，如删除后，此元素依然存在
    - CONTRARY_GETVAL = "contrary_getval" # 检查点关键字contrary_getval: 相反值检查点，如果对比成功，说明失败
    - DEFAULT_CHECK = "default_check" # 默认检查点，就是查找页面元素
    - COMPARE = "compare" # 历史数据和实际数据对比
- 实时打印日志

 
