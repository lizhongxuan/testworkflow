# 测试流水线流程图

```plaintext
+-------------------+
| - 生成全局请求ID    |
+-------------------+
          |
          v
      搭建测试目标
+-------------------+
| - 运行PG容器       |
| - 托管中间件平台    |
| - 保存实例信息      |
| - 保存日志和状态    |
+-------------------+
          |
          v
     运行测试脚本
+-------------------+
| - 获取Shell内容    |
| - 运行Shell脚本    |
| - 保存日志和状态    |
+-------------------+
          |
          v
    运行混沌测试(可选) 
+-------------------+
| - 启动混沌测试      |
| - 保存日志和状态     |
+-------------------+
          |
          v
    检测测试目标状态
+-------------------+
| - 检查目标状态      |
| - 重试机制         |
| - 保存日志和状态    |
+-------------------+