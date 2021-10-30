# lecture-information-crawler
# 学术报告讲座信息抓取
## 实现功能
### 后端到前端：
1. Get the html code of the website: modify the request header; visit it as an ordinary browser; and use the BS library to parse the HTML code(获取网站html代码：修改请求头，伪装成普通浏览器访问，并用bs库解析HTML代码)
2. Select the information needed: use the functional functions and regular expressions in the RE library to identify and crawl the needed content of the html code.(爬取需要的信息：使用re库中的功能函数和正则表达式，对html代码内容实现识别和抓取)
3. Store the data: use Sqlite3 to store data; build database -> insert tables -> insert data line by line.(储存数据库：使用sqlite3装数据，建库、插表、插数据)
4. Personalized information in database, such as sorting data by (lectures')start time / publication time / keyword filtering.(对数据库信息进行个性化处理，如：按开始时间排序、按公布时间排序、关键字过滤)
5. Develop a web side showing information: users can click the "search engine" button, and the server will run the program; update database; present it on the web.(Web端展现数据库信息：flask框架搭建web程序，通过函数调用更新数据库信息并呈现在web上)

### 前端到后端：
1.	用户点击开启爬虫程序，web调用封装好的py文件，刷新数据库并呈现在web上
2.	用户输入关键字，web拿到关键字跳转到指定网站，自动在指定网站进行查询，展示所有与关键字相关的讲座或学术报告
## 网页展示
### 首页
![image](https://user-images.githubusercontent.com/78016917/117303773-a96dfe80-aeaf-11eb-8c39-f998f8412a2a.png)
#### 爬取成功：
![image](https://user-images.githubusercontent.com/78016917/117303945-cf939e80-aeaf-11eb-8b4c-96b8cba5337e.png)
### 查找学术信息
![image](https://user-images.githubusercontent.com/78016917/117304004-de7a5100-aeaf-11eb-9b38-2b10a6bd0ccc.png)
#### 在第一个输入框输入关键字：“人工智能”后转跳效果：
![image](https://user-images.githubusercontent.com/78016917/117304071-edf99a00-aeaf-11eb-8ab3-7107a3ea33ac.png)
### 讲座信息表展示页
![image](https://user-images.githubusercontent.com/78016917/117304132-fce04c80-aeaf-11eb-8c15-66aedcdc4899.png)
#### 表中链接可以正常转跳
