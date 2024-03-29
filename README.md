<h1 align="center">fastapi_template</h1>

## 此仓库已于2024年3月14日迁移至组织
[点击跳转](https://github.com/ttutils/fastapi_template)

此项目是根据[@buyfakett](https://github.com/buyfakett)的fastapi使用习惯的模板仓库

项目目录：

```bash
.
├── api
│   ├── base.py				# 封装response
│   └── test.py				# 测试类
├── config
│   └── config.yaml				# 配置文件
├── Dockerfile
├── main.py					# 启动文件
├── models
│   └── test.py				# 数据库模型类
├── README.md
├── requirements.txt		# 依赖
├── settings.py				# ORM数据库连接文件
└── util
    └── yaml_util.py		# yaml配置

```



- 该仓库使用postgres作为数据库

- 配置文件放在config目录下，具体使用的时候`read_yaml('key', 'file_name')`

### 执行数据库迁移

```bash
# 第一次
aerich init -t settings.TORTOISE_ORM
aerich init-db
```

```bash
# 后面
aerich migrate
aerich upgrade
```
