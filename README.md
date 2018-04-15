###  json-server

这些数据是 my-customer 需要连接的数据

启动json-server 

$ git clone ...

$ cd json-server

$ npm install

$ npm run json:server


###

# 用户管理系统  开发日志

#### 
1. 下载postman ---需要翻墙，如果不翻墙  [https://blog.csdn.net/water_0815/article/details/53263643]

2. json数据   [http://jsonplaceholder.typicode.com/]

3. json-server 搭建[https://github.com/typicode/json-server]

4. $  cnpm install -g json-server 

5. $  mkdir JSONSERVER

6. $  npm init 

7. $  npm install json-server --save 

8. Start JSON Server 

```s
    $ json-server --watch db.json

    或者 在 package.json 中加入

    "scripts": {
        "json:server": "json-server --watch db.json"
    },
```

### 创建一个 db.json

```json
{
    "users":[
        {
            "name":"Henry",
            "phone":"333-444-555",
            "email":"isshaohai@163.com",
            "id":1,
            "age":30,
            "companyId":1
        },
        {
            "name":"Bucky",
            "phone":"333-444-555",
            "email":"Bucky@163.com",
            "id":2,
            "age":30,
            "companyId":2
        },
        {
            "name":"Emily",
            "phone":"333-444-555",
            "email":"Emily@163.com",
            "id":3,
            "age":30,
            "companyId":3
        },
        {
            "name":"Elyse",
            "phone":"333-444-555",
            "email":"Elyse@163.com",
            "id":4,
            "age":30,
            "companyId":3
        }
    ],
    "companies":[
        {
            "id":1,
            "name":"Apply",
            "description":"Apple is good!"
        },
        {
            "id":2,
            "name":"Microsoft",
            "description":"Apple is good!"
        },
        {
            "id":3,
            "name":"Google",
            "description":"Apple is good!"
        }
    ]
}
```

### 启动 json:server

```s
    $ npm run json:server 
```


### 打开浏览器

```
输入：localhsot:3000  

输入：localhost:3000/users     拿到 users 数据
输入：localhost:3000/companies 拿到 companies 数据

// 获取所有用户信息
http://localhost:3000/users

// 获取id为1的用户信息
http://localhost:3000/users/1

// 获取公司的所有信息
http://localhost:3000/companies

// 获取单个公司的信息
http://localhost:3000/companies/1

// 获取所有公司id为3的用户
http://localhost:3000/companies/3/users

// 根据公司名字获取信息
http://localhost:3000/companies?name=Microsoft

// 根据多个名字获取公司信息
http://localhost:3000/companies?name=Microsoft&name=Apple

// 获取一页中只有两条数据
http://localhost:3000/companies?_page=1&_limit=2

// 升序排序 asc升序 desc降序
http://localhost:3000/companies?_sort=name&_order=asc

// 获取年龄30及以上的
http://localhost:3000/users?age_gte=30

// 获取年龄在30到40之间
http://localhost:3000/users?age_gte=30&age_lte=40

// 搜索用户信息
http://localhost:3000/users?q=h

```

## 使用 postman  请求数据接口 

![Image]()





