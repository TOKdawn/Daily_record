### users （用户）
1. login
    登录(github)

    `get /passport/github`

1. logout
 
    注销

    `get /user/logout`


1. login
 
    注册

    `get /user/logout`



1. Get an user information（需验证）

    获取用户信息

    ` GET  /user/:uid`


    返回参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    | id         | number  |  用户id  |
    | name       | srting  |  用户名   |
    | role       | number  |  用户角色 |
    
    //1登录 ,0未登录,2管理员
    
    获取用户自己的信息
    
   ` GET  /user`
   
2. get results

	获取某用户成绩
	
  ` GET  /user/results/:uid`

   
 
### exam （考试）

1. List exam

    展示所有试卷

    ` GET  /exam`


3. Create a exam （需验证）

    创建一个试卷

    ` POST  /exam`
 
    请求参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    | title       | string  |  试卷名 |
    | describe   | string    |  描述   |
    
 

  

6. Delete a exam （需验证）

    删除一个自己的试卷

    ` DELETE  exam/:eid`


7.  List scores in a volume

    返回一个给定id的试卷里的所有试题

    ` GET  /exam/:eid/question`

 
     返回参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    | data      | array  |  试题列表   |
    
  
8. Add a score to a volume （需验证）

    往一个特定试卷里添加一个试题

    `POST  /exam/:eid/choose `

    请求参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    | qid        | number  |  试题id  |
  

8. Add a score to a volume （需验证）

    往一个特定试卷里添加一个听力题

    `POST  /exam/:eid/hear `

    请求参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    | qid        | number  |  试题id  |
  


9. Show all choose 

	显示所有的选择题
	
	`GET /choose`
	
9. Show all question 

	显示所有的听力题
	
	`GET /question`
	



## question

9.   `POST  /question/choose`

	 上传一个试题

	   请求参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    |    title  	|  string |  题目    |
    |    data    |   object |   选项   | 
  




10. `POST  /question/hear` 

		
	上传一个听力题
	
	  请求参数

    | 参数        | 类型    |  描述    |
    | --------   | -----:  | :----:  |
    |    title  |  string |  题目    |
    |    data    |   object   |   选项 | 
  	|    url    |   string   |  音频地址|

11. `POST /upload`

	上传一段音频
	


	
	
	

  
  