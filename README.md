# 句子包

一言开源社区官方提供的语句库，系 `hitokoto.cn` 数据打包集合。语句接口默认使用此库。

# 项目介绍
## 本项目数据完全基于 https://github.com/hitokoto-osc/sentences-bundle 库
## 如有数据更新请自行前往原库下载sentences文件夹内json文件替换
## windows自建本地无限速一言api接口，添加基于Fastapi运行的HTTP GET接口，测试运行于Python3.10.9510环境下，建议运行在3.10版本，linux请自行修改启动脚本

## 使用须知

1. 本库遵循 AGPL 开源授权，您在使用本库时需要遵循 AGPL 授权的相关规定。这通常意味着：您在使用、分发、修改、扩充等涉及本库的操作时您需要开源您的修改作品。
*  除我们提供的超链接调用方式不受 AGPL 的开源，传染影响，其余使用方式都需要遵循 AGPL 授权。

## 使用方法

1. 下载本仓库到本地你想存放的目录
2. pip安装poetry
3. 点击安装poetry依赖脚本文件创建该目录的虚拟环境
4. 编辑config.json文件，本地部署将host修改成127.0.0.1，局域网部署将host修改成0.0.0.0，post自定义你想要的端口
5. 点击start脚本文件运行api
6. 使用接口为 http://host:port/HITOKOTO ，获取一条随机一言

## 调用方法
`GET`
## 参数说明
参数名|类型|含义
-|-|-
data|string|获取你想要的数据格式
空or未匹配参数|null|默认返回 JSON 格式数据

### 数据格式说明
参数值|含义
-|-
json|返回 JSON 格式数据
text|返回纯文字一言
空or未匹配参数|默认返回 JSON 格式数据

默认参数返回值示例
```json
{
    "code":200,
    "message":"success",
    "data":{
        "id":5169,
        "uuid":"833a4fb8-73e7-473a-ac81-7d0398630dd6",
        "hitokoto":"没心没肺，活着不累。",
        "type":"f",
        "from":"网络",
        "from_who":null,
        "creator":"2247",
        "creator_uid":5148,
        "reviewer":4756,
        "commit_from":"web",
        "created_at":"1582967894",
        "length":10
    }
}
```
