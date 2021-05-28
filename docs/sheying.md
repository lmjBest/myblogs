## 访问IP:端口

* `http://121.5.115.185:8080`

## 视频彩铃

### 5G视频彩铃制作列表

> 接口简介：

* 根据当前账号查询视频彩铃记录，接口所用如下图：


> 请求URL：

* /front/video/myList

> 请求方式：

* POST

> 请求参数：

|  参数名  | 必选 |  类型  | 说明 |   备注   |
| :------: | :--: | :----: | :--: | :------: |
| username |  是  | string | 账号 | zhangsan |

> 返回示例：

```json
{
    "msg": "操作成功",
    "code": 0,
    "data": [
        {
            "createTime": "2021-04-07 22:02:44",
            "updateTime": "2021-04-07 22:02:44",
            "id": 1, //视频彩铃id
            "username": "zhangsan", //账号
            "videoName": "测试视频彩铃名称", //视频彩铃名称
            "coverImage": "/profile/upload/2021/04/07/0d9f341c-05e0-4cfd-8ec2-d88670d32dd4.png",//封面图片地址 前缀8089
            "phone": "18912349876",
            "isDel": 0,
            "videoUrl": "/profile/upload/2021/04/07/40fd0857-54c6-4a8e-888d-e98aa53ccc2e.mp4"//视频地址 
        }
    ]
}
```

> 错误示例：

```json
{
    "msg": "账号不能为空",
    "code": 500
}
```

### 5G视频彩铃制作编辑页面

> 接口简介：

* 进入编辑页面，根据id查询当前编辑页面展示数据，如下图：

  ![image-20210408193039954](C:\Users\49179\AppData\Roaming\Typora\typora-user-images\image-20210408193039954.png)

> 请求URL：

* /front/video/get

> 请求方式：

* POST

> 请求参数：

| 参数名 | 必选 | 类型 |    说明    | 备注 |
| :----: | :--: | :--: | :--------: | :--: |
|   id   |  是  | int  | 视频彩铃id |  1   |

> 返回示例：

```json
{
    "msg": "操作成功",
    "code": 0,
    "data": {
        "createTime": "2021-04-08 16:49:29",
        "updateTime": "2021-04-08 16:49:29",
        "id": 2,
        "username": "caozhi",
        "videoName": "5g",
        "coverImage": "/profile/upload/2021/04/08/c5be960f-a47f-46ad-a45b-048d0ea26532.jpg",
        "phone": "555",
        "isDel": 0,
        "videoUrl": "/profile/upload/2021/04/08/4b14e8d2-10df-4052-b5b5-2b6bbba2bbe6.mp4"
    }
}
```

> 错误示例：

```json
{
    "msg": "id不能为空",
    "code": 500
}
```

### 5G视频彩铃制作保存

> 接口简介：

* 5G视频彩铃制作编辑页面修改后的保存接口

> 请求URL：

* /front/video/save

> 请求方式：

* POST

> 请求参数：

|  参数名   | 必选 |  类型  |     说明     |    备注     |
| :-------: | :--: | :----: | :----------: | :---------: |
| coverFile |  是  |  file  | 封面图片文件 |  xxxx.jpg   |
| videoFile |  是  |  file  |   视频文件   |  xxxx.mp4   |
|    id     |  是  |  int   |  视频彩铃id  |      1      |
| username  |  是  | string |     账号     |  zhangsan   |
|   phone   |  否  | string |   手机号码   | 18912349876 |
| videoName |  是  | string | 视频彩铃名称 | 为你唱这首  |

> 返回示例：

```json
{
    "msg": "操作成功",
    "code": 0
}
```

> 错误示例：

```json
{
    "msg": "id不能为空",
    "code": 500
}
```

### 5G视频彩铃制作删除

> 接口简介：

* 删除功能，如下图

![image-20210408193605421](C:\Users\49179\AppData\Roaming\Typora\typora-user-images\image-20210408193605421.png)

> 请求URL：

* /front/video/delete

> 请求方式：

* POST

> 请求参数：

| 参数名 | 必选 | 类型 |    说明    | 备注 |
| :----: | :--: | :--: | :--------: | :--: |
|   id   |  是  | int  | 视频彩铃id |  1   |

> 返回示例：

```json
{
    "msg": "操作成功",
    "code": 0
}
```

> 错误示例：

```json
{
    "msg": "id不能为空",
    "code": 500
}
```
