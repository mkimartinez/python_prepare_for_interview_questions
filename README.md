This is english translated version of the original ( https://github.com/kenwoodjw/python_interview_question ) chinese repository.
With more python interview questions. 
<!-- TOC -->
- [Python-Basics](#python-basics)
  * [Working with files](#working-with-files)
    + [1. There is a json file with about 10K lines of data, write a function to read and process the data](#1-there-is-a-json-file-with-about-10k-lines-of-data--write-a-function-to-read-and-process-the-data)
    + [2.Fill in the missing code](#2fill-in-the-missing-code)
  * [Modules and Libraries](#modules-and-libraries)
    + [3.Enter the date， Output the day, month and year？](#3enter-the-date--output-the-day--month-and-year-)
    + [4.write a function to shuffle elements of a sorted list？](#4write-a-function-to-shuffle-elements-of-a-sorted-list-)
  * [Data types](#data-types)
    + [5.Given a dictionary d= {'a':24,'g':52,'i':12,'k':33}; Sort based on values?](#5given-a-dictionary-d----a--24--g--52--i--12--k--33---sort-based-on-values-)
    + [6. Dictionary Comprehensions](#6-dictionary-comprehensions)
    + [7.Write a function to reverse a given string "aStr"?](#7write-a-function-to-reverse-a-given-string--astr--)
    + [8. Process the string "k: 1 | k1: 2 | k2: 3 | k3: 4" into a dictionary {k: 1, k1: 2, ...}](#8-process-the-string--k--1---k1--2---k2--3---k3--4--into-a-dictionary--k--1--k1--2---)
    + [9. Please sort by the age of the elements in alist from largest to smallest](#9-please-sort-by-the-age-of-the-elements-in-alist-from-largest-to-smallest)
    + [10.What is the output of the following code？](#10what-is-the-output-of-the-following-code-)
    + [11.Write a list generator， to generate an arithmetic sequence whose common difference is 11](#11write-a-list-generator--to-generate-an-arithmetic-sequence-whose-common-difference-is-11)
    + [12. Given two lists, write a function to find out the same elements and different elements from the two lists](#12-given-two-lists--write-a-function-to-find-out-the-same-elements-and-different-elements-from-the-two-lists)
    + [13. Write python code to delete duplicate elements from a list？](#13-write-python-code-to-delete-duplicate-elements-from-a-list-)
    + [14.Given two lists A，B ,Find elements that are similar and different in list A and list B](#14given-two-lists-a-b--find-elements-that-are-similar-and-different-in-list-a-and-list-b)
  * [Enterprise interview questions](#enterprise-interview-questions)
    - [15.What is the difference between new style class and the classic class in python？](#15what-is-the-difference-between-new-style-class-and-the-classic-class-in-python-)
    + [16.What are built-in data types in Python？](#16what-are-built-in-data-types-in-python-)
    + [17. How to implement singleton mode in Python? Please write two ways of implementation?](#17-how-to-implement-singleton-mode-in-python--please-write-two-ways-of-implementation-)
        + [18. Write a class with a function to reverse the input. For example; -123 --> -321](#18-write-a-class-with-a-function-to-reverse-the-input-for-example---123------321)
    + [19. Design a function to traverse a directory and grap all the files with the specified extension](#19-design-a-function-to-traverse-a-directory-and-grap-all-the-files-with-the-specified-extension)
    + [20.Calculate the sum of (1-100) using one line of code](#20calculate-the-sum-of--1-100--using-one-line-of-code)
    + [21.Write a Python function to delete elements when traversing a list](#21write-a-python-function-to-delete-elements-when-traversing-a-list)
    + [22. String operation problems](#22-string-operation-problems)
    + [23.Mutable and Immutable data types](#23mutable-and-immutable-data-types)
    + [24.What is the difference between "is" and "==" in python？](#24what-is-the-difference-between--is--and------in-python-)
    + [25. Find all odd numbers in a list and construct a new list](#25-find-all-odd-numbers-in-a-list-and-construct-a-new-list)
    + [26. write one line of code to generate 1+2+3+10248](#26-write-one-line-of-code-to-generate-1-2-3-10248)
    + [27.Variable scopes in python？（Variable search order)](#27variable-scopes-in-python--variable-search-order-)
    + [28. The string "123" is converted to '123' without using built-in functions such as 'int()'](#28-the-string--123--is-converted-to--123--without-using-built-in-functions-such-as--int---)
    + [29.Given an array of integers](#29given-an-array-of-integers)
    + [30.python code to remove duplicate element from a list](#30python-code-to-remove-duplicate-element-from-a-list)
    + [31. Count the 10 most frequent words in a text？](#31-count-the-10-most-frequent-words-in-a-text-)
    + [32.Please write a function that meets the following conditions](#32please-write-a-function-that-meets-the-following-conditions)
    + [33.Use a single list generator to generate a new list](#33use-a-single-list-generator-to-generate-a-new-list)
    + [34.Generate the following list [1,4,9,16,25,36,49,64,81,100] using one line of code](#34generate-the-following-list--1-4-9-16-25-36-49-64-81-100--using-one-line-of-code)
    + [35.Write a function that takes the year, month and day as the input and outputs the day of the year？](#35write-a-function-that-takes-the-year--month-and-day-as-the-input-and-outputs-the-day-of-the-year-)
    + [36.Merge two ordered list l1,l2 without using extend function](#36merge-two-ordered-list-l1-l2-without-using-extend-function)
    + [37.Given an array of arbitrary length, implement a function](#37given-an-array-of-arbitrary-length--implement-a-function)
    + [38. Write a function to find the second largest number in an integer array](#38-write-a-function-to-find-the-second-largest-number-in-an-integer-array)
    + [39.What is the output of the following function？](#39what-is-the-output-of-the-following-function-)
    + [40. Count the number of occurrences of characters in a string](#40-count-the-number-of-occurrences-of-characters-in-a-string)
    + [41. What are some specific use cases of super() function](#41-what-are-some-specific-use-cases-of-super---function)
- [Advanced Python](#advanced-python)
  * [Metaclass](#metaclass)
    + [42. What is the difference between class instance methods and static methods?](#42-what-is-the-difference-between-class-instance-methods-and-static-methods-)
    + [44.Write a class that supports as many operators as possible?](#44write-a-class-that-supports-as-many-operators-as-possible-)
    + [45.Describe the drawbacks of Cython，Pypy Cpython Numba](#45describe-the-drawbacks-of-cython-pypy-cpython-numba)
    + [46.Please describe the difference and connection between abstract class and interface class](#46please-describe-the-difference-and-connection-between-abstract-class-and-interface-class)
    + [47. How to dynamically get and set the attributes of an object in Python？](#47-how-to-dynamically-get-and-set-the-attributes-of-an-object-in-python-)
  * [Memory management and garbage collection mechanism](#memory-management-and-garbage-collection-mechanism)
    + [48.What operations will cause Python memory overflow, how to deal with those causes？](#48what-operations-will-cause-python-memory-overflow--how-to-deal-with-those-causes-)
    + [49.Regarding Python memory management, which of the following statements is wrong  B](#49regarding-python-memory-management--which-of-the-following-statements-is-wrong--b)
    + [50.Python's memory management mechanism and tuning methods？](#50python-s-memory-management-mechanism-and-tuning-methods-)
    + [51. What is a memory leak? How to avoid it?](#51-what-is-a-memory-leak--how-to-avoid-it-)
  * [Python functions](#python-functions)
    + [52.What are common list comprehensions？](#52what-are-common-list-comprehensions-)
    + [53.Describe the difference among read、readline、readlines？](#53describe-the-difference-among-read-readline-readlines-)
    + [54.What is a Hash function？](#54what-is-a-hash-function-)
    + [55.Python function overloading mechanism？](#55python-function-overloading-mechanism-)
    + [56.Write a function to find the second largest number in an integer array](#56write-a-function-to-find-the-second-largest-number-in-an-integer-array)
    + [57.Write a decorator function to determine the current time](#57write-a-decorator-function-to-determine-the-current-time)
    + [58. Write a function to filter items from a list using the built-in filter() function？](#58-write-a-function-to-filter-items-from-a-list-using-the-built-in-filter---function-)
    + [59. The four principles of writing a function in Python](#59-the-four-principles-of-writing-a-function-in-python)
    + [60. Is the function call parameter passed by value or by reference？](#60-is-the-function-call-parameter-passed-by-value-or-by-reference-)
    + [61.How to set a global variable in function?](#61how-to-set-a-global-variable-in-function-)
    + [62. Understanding of default parameters ？](#62-understanding-of-default-parameters--)
    + [63. How to limit IP access in MYSQL？](#63-how-to-limit-ip-access-in-mysql-)
    + [64.Decorators with parameters?](#64decorators-with-parameters-)
    + [65. Why function names can be used as parameters?](#65-why-function-names-can-be-used-as-parameters-)
- [Python program to illustrate functions can be passed as arguments to other functions](#python-program-to-illustrate-functions-can-be-passed-as-arguments-to-other-functions)
    + [66. What is the role of the pass statement in Python？](#66-what-is-the-role-of-the-pass-statement-in-python-)
    + [67. Given the following code, what will be the output of print(c), why?](#67-given-the-following-code--what-will-be-the-output-of-print-c---why-)
    + [68. What are different way of Swaping the values of two variables？](#68-what-are-different-way-of-swaping-the-values-of-two-variables-)
    + [69. Using map() and reduce() functions in Python？](#69-using-map---and-reduce---functions-in-python-)
    + [70.How the callback function communicates?](#70how-the-callback-function-communicates-)
    + [71. What are the main built-in data types in Python? What is the output of print dir (‘a’)?](#71-what-are-the-main-built-in-data-types-in-python--what-is-the-output-of-print-dir---a---)
    + [72.What is the output of map(lambda x:xx，[y for y in range(3)])？](#72what-is-the-output-of-map-lambda-x-xx--y-for-y-in-range-3----)
    + [73. What is the detailed use cases of the following functions hasattr(), getattr(), setattr()？](#73-what-is-the-detailed-use-cases-of-the-following-functions-hasattr----getattr----setattr---)
    + [74.Solve the factorial function using one line of code？](#74solve-the-factorial-function-using-one-line-of-code-)
    + [75. What is a lambda function？ What are the benefits of using lambda function？](#75-what-is-a-lambda-function--what-are-the-benefits-of-using-lambda-function-)
    + [76. What are the termination conditions for recursive functions？](#76-what-are-the-termination-conditions-for-recursive-functions-)
    + [77.What will be the output of the following code? Please explain.](#77what-will-be-the-output-of-the-following-code--please-explain)
- [Method 1:](#method-1-)
- [Method 2:](#method-2-)
    + [78. What is a lambda function? What are the benefits? Write an anonymous function to find the sum of two numbers](#78-what-is-a-lambda-function--what-are-the-benefits--write-an-anonymous-function-to-find-the-sum-of-two-numbers)
  * [Python Design Patterns](#python-design-patterns)
    + [79. Understanding of design patterns, briefly describe the design patterns you understand？](#79-understanding-of-design-patterns--briefly-describe-the-design-patterns-you-understand-)
    + [80.Write one singleton class](#80write-one-singleton-class)
    + [81.What are some common usecases of singleton design pattern？](#81what-are-some-common-usecases-of-singleton-design-pattern-)
        - [81.单例模式的应用场景有那些？](#81单例模式的应用场景有那些)
        - [82.用一行代码生成[1,4,9,16,25,36,49,64,81,100]](#82用一行代码生成149162536496481100)
        - [83.对装饰器的理解，并写出一个计时器记录方法执行性能的装饰器？](#83对装饰器的理解并写出一个计时器记录方法执行性能的装饰器)
        - [84.解释以下什么是闭包？](#84解释以下什么是闭包)
        - [85.函数装饰器有什么作用？](#85函数装饰器有什么作用)
        - [86.生成器，迭代器的区别？](#86生成器迭代器的区别)
        - [87.X是什么类型?](#87x是什么类型)
        - [88.请用一行代码 实现将1-N 的整数列表以3为单位分组](#88请用一行代码-实现将1-n-的整数列表以3为单位分组)
        - [89.Python中yield的用法?](#89python中yield的用法)
    - [面向对象](#面向对象)
        - [90.Python中的可变对象和不可变对象？](#90python中的可变对象和不可变对象)
        - [91.Python的魔法方法](#91python的魔法方法)
        - [92.面向对象中怎么实现只读属性?](#92面向对象中怎么实现只读属性)
        - [93.谈谈你对面向对象的理解？](#93谈谈你对面向对象的理解)
    - [正则表达式](#正则表达式)
        - [94.请写出一段代码用正则匹配出ip？](#94请写出一段代码用正则匹配出ip)
        - [95.a = “abbbccc”，用正则匹配为abccc,不管有多少b，就出现一次？](#95a--abbbccc用正则匹配为abccc不管有多少b就出现一次)
        - [96.Python字符串查找和替换？](#96python字符串查找和替换)
        - [97.用Python匹配HTML g tag的时候，<.> 和 <.*?> 有什么区别](#97用python匹配html-g-tag的时候-和--有什么区别)
        - [98.正则表达式贪婪与非贪婪模式的区别？](#98正则表达式贪婪与非贪婪模式的区别)
        - [99.写出开头匹配字母和下划线，末尾是数字的正则表达式？](#99写出开头匹配字母和下划线末尾是数字的正则表达式)
        - [100.正则表达式操作](#100正则表达式操作)
        - [101.请匹配出变量A 中的json字符串。](#101请匹配出变量a-中的json字符串)
        - [102.怎么过滤评论中的表情？](#102怎么过滤评论中的表情)
        - [103.简述Python里面search和match的区别](#103简述python里面search和match的区别)
        - [104.请写出匹配ip的Python正则表达式](#104请写出匹配ip的python正则表达式)
        - [105.Python里match与search的区别？](#105python里match与search的区别)
    - [系统编程](#系统编程)
        - [106.进程总结](#106进程总结)
        - [107.谈谈你对多进程，多线程，以及协程的理解，项目是否用？](#107谈谈你对多进程多线程以及协程的理解项目是否用)
        - [108.Python异常使用场景有那些？](#108python异常使用场景有那些)
        - [109.多线程共同操作同一个数据互斥锁同步？](#109多线程共同操作同一个数据互斥锁同步)
        - [110.什么是多线程竞争？](#110什么是多线程竞争)
        - [111.请介绍一下Python的线程同步？](#111请介绍一下python的线程同步)
        - [112.解释以下什么是锁，有哪几种锁？](#112解释以下什么是锁有哪几种锁)
        - [113.什么是死锁？](#113什么是死锁)
        - [114.多线程交互访问数据，如果访问到了就不访问了？](#114多线程交互访问数据如果访问到了就不访问了)
        - [115.什么是线程安全，什么是互斥锁？](#115什么是线程安全什么是互斥锁)
        - [116.说说下面几个概念：同步，异步，阻塞，非阻塞？](#116说说下面几个概念同步异步阻塞非阻塞)
        - [117.什么是僵尸进程和孤儿进程？怎么避免僵尸进程？](#117什么是僵尸进程和孤儿进程怎么避免僵尸进程)
        - [118.python中进程与线程的使用场景？](#118python中进程与线程的使用场景)
        - [119.线程是并发还是并行，进程是并发还是并行？](#119线程是并发还是并行进程是并发还是并行)
        - [120.并行(parallel)和并发（concurrency)?](#120并行parallel和并发concurrency)
        - [121.IO密集型和CPU密集型区别？](#121io密集型和cpu密集型区别)
        - [122.python asyncio的原理？](#122python-asyncio的原理)
    - [网络编程](#网络编程)
        - [123.怎么实现强行关闭客户端和服务器之间的连接?](#123怎么实现强行关闭客户端和服务器之间的连接)
        - [124.简述TCP和UDP的区别以及优缺点?](#124简述tcp和udp的区别以及优缺点)
        - [125.简述浏览器通过WSGI请求动态资源的过程?](#125简述浏览器通过wsgi请求动态资源的过程)
        - [126.描述用浏览器访问www.baidu.com的过程](#126描述用浏览器访问wwwbaiducom的过程)
        - [127.Post和Get请求的区别?](#127post和get请求的区别)
        - [128.cookie 和session 的区别？](#128cookie-和session-的区别)
        - [129.列出你知道的HTTP协议的状态码，说出表示什么意思？](#129列出你知道的http协议的状态码说出表示什么意思)
        - [130.请简单说一下三次握手和四次挥手？](#130请简单说一下三次握手和四次挥手)
        - [131.说一下什么是tcp的2MSL？](#131说一下什么是tcp的2msl)
        - [132.为什么客户端在TIME-WAIT状态必须等待2MSL的时间？](#132为什么客户端在time-wait状态必须等待2msl的时间)
        - [133.说说HTTP和HTTPS区别？](#133说说http和https区别)
        - [134.谈一下HTTP协议以及协议头部中表示数据类型的字段？](#134谈一下http协议以及协议头部中表示数据类型的字段)
        - [135.HTTP请求方法都有什么？](#135http请求方法都有什么)
        - [136.使用Socket套接字需要传入哪些参数 ？](#136使用socket套接字需要传入哪些参数-)
        - [137.HTTP常见请求头？](#137http常见请求头)
        - [138.七层模型？](#138七层模型)
        - [139.url的形式？](#139url的形式)
- [Web](#web)
    - [Flask](#flask)
        - [140.对Flask蓝图(Blueprint)的理解？](#140对flask蓝图blueprint的理解)
        - [141.Flask 和 Django 路由映射的区别？](#141flask-和-django-路由映射的区别)
    - [Django](#django)
        - [142.什么是wsgi,uwsgi,uWSGI?](#142什么是wsgiuwsgiuwsgi)
        - [143.Django、Flask、Tornado的对比？](#143djangoflasktornado的对比)
        - [144.CORS 和 CSRF的区别？](#144cors-和-csrf的区别)
        - [145.Session,Cookie,JWT的理解](#145sessioncookiejwt的理解)
        - [146.简述Django请求生命周期](#146简述django请求生命周期)
        - [147.用的restframework完成api发送时间时区](#147用的restframework完成api发送时间时区)
        - [148.nginx,tomcat,apach到都是什么？](#148nginxtomcatapach到都是什么)
        - [149.请给出你熟悉关系数据库范式有哪些，有什么作用？](#149请给出你熟悉关系数据库范式有哪些有什么作用)
        - [150.简述QQ登陆过程](#150简述qq登陆过程)
        - [151.post 和 get的区别?](#151post-和-get的区别)
        - [152.项目中日志的作用](#152项目中日志的作用)
        - [153.django中间件的使用？](#153django中间件的使用)
        - [154.谈一下你对uWSGI和nginx的理解？](#154谈一下你对uwsgi和nginx的理解)
        - [155.Python中三大框架各自的应用场景？](#155python中三大框架各自的应用场景)
        - [156.Django中哪里用到了线程？哪里用到了协程？哪里用到了进程？](#156django中哪里用到了线程哪里用到了协程哪里用到了进程)
        - [157.有用过Django REST framework吗？](#157有用过django-rest-framework吗)
        - [158.对cookies与session的了解？他们能单独用吗？](#158对cookies与session的了解他们能单独用吗)
    - [爬虫](#爬虫)
        - [159.试列出至少三种目前流行的大型数据库](#159试列出至少三种目前流行的大型数据库)
        - [160.列举您使用过的Python网络爬虫所用到的网络数据包?](#160列举您使用过的python网络爬虫所用到的网络数据包)
        - [161.爬取数据后使用哪个数据库存储数据的，为什么？](#161爬取数据后使用哪个数据库存储数据的为什么)
        - [162.你用过的爬虫框架或者模块有哪些？优缺点？](#162你用过的爬虫框架或者模块有哪些优缺点)
        - [163.写爬虫是用多进程好？还是多线程好？](#163写爬虫是用多进程好还是多线程好)
        - [164.常见的反爬虫和应对方法？](#164常见的反爬虫和应对方法)
        - [165.解析网页的解析器使用最多的是哪几个?](#165解析网页的解析器使用最多的是哪几个)
        - [166.需要登录的网页，如何解决同时限制ip，cookie,session](#166需要登录的网页如何解决同时限制ipcookiesession)
        - [167.验证码的解决?](#167验证码的解决)
        - [168.使用最多的数据库，对他们的理解？](#168使用最多的数据库对他们的理解)
        - [169.编写过哪些爬虫中间件？](#169编写过哪些爬虫中间件)
        - [170.“极验”滑动验证码如何破解？](#170极验滑动验证码如何破解)
        - [171.爬虫多久爬一次，爬下来的数据是怎么存储？](#171爬虫多久爬一次爬下来的数据是怎么存储)
        - [172.cookie过期的处理问题？](#172cookie过期的处理问题)
        - [173.动态加载又对及时性要求很高怎么处理？](#173动态加载又对及时性要求很高怎么处理)
        - [174.HTTPS有什么优点和缺点？](#174https有什么优点和缺点)
        - [175.HTTPS是如何实现安全传输数据的？](#175https是如何实现安全传输数据的)
        - [176.TTL，MSL，RTT各是什么？](#176ttlmslrtt各是什么)
        - [177.谈一谈你对Selenium和PhantomJS了解](#177谈一谈你对selenium和phantomjs了解)
        - [178.平常怎么使用代理的 ？](#178平常怎么使用代理的-)
        - [179.存放在数据库(redis、mysql等)。](#179存放在数据库redismysql等)
        - [180.怎么监控爬虫的状态?](#180怎么监控爬虫的状态)
        - [181.描述下scrapy框架运行的机制？](#181描述下scrapy框架运行的机制)
        - [182.谈谈你对Scrapy的理解？](#182谈谈你对scrapy的理解)
        - [183.怎么样让 scrapy 框架发送一个 post 请求（具体写出来）](#183怎么样让-scrapy-框架发送一个-post-请求具体写出来)
        - [184.怎么监控爬虫的状态 ？](#184怎么监控爬虫的状态-)
        - [185.怎么判断网站是否更新？](#185怎么判断网站是否更新)
        - [186.图片、视频爬取怎么绕过防盗连接](#186图片视频爬取怎么绕过防盗连接)
        - [187.你爬出来的数据量大概有多大？大概多长时间爬一次？](#187你爬出来的数据量大概有多大大概多长时间爬一次)
        - [188.用什么数据库存爬下来的数据？部署是你做的吗？怎么部署？](#188用什么数据库存爬下来的数据部署是你做的吗怎么部署)
        - [189.增量爬取](#189增量爬取)
        - [190.爬取下来的数据如何去重，说一下scrapy的具体的算法依据。](#190爬取下来的数据如何去重说一下scrapy的具体的算法依据)
        - [191.Scrapy的优缺点?](#191scrapy的优缺点)
        - [192.怎么设置爬取深度？](#192怎么设置爬取深度)
        - [193.scrapy和scrapy-redis有什么区别？为什么选择redis数据库？](#193scrapy和scrapy-redis有什么区别为什么选择redis数据库)
        - [194.分布式爬虫主要解决什么问题？](#194分布式爬虫主要解决什么问题)
        - [195.什么是分布式存储？](#195什么是分布式存储)
        - [196.你所知道的分布式爬虫方案有哪些？](#196你所知道的分布式爬虫方案有哪些)
        - [197.scrapy-redis，有做过其他的分布式爬虫吗？](#197scrapy-redis有做过其他的分布式爬虫吗)
- [数据库](#数据库)
    - [MySQL](#mysql)
        - [198.主键 超键 候选键 外键](#198主键-超键-候选键-外键)
        - [199.视图的作用，视图可以更改么？](#199视图的作用视图可以更改么)
        - [200.drop,delete与truncate的区别](#200dropdelete与truncate的区别)
        - [201.索引的工作原理及其种类](#201索引的工作原理及其种类)
        - [202.连接的种类](#202连接的种类)
        - [203.数据库优化的思路](#203数据库优化的思路)
        - [204.存储过程与触发器的区别](#204存储过程与触发器的区别)
        - [205.悲观锁和乐观锁是什么？](#205悲观锁和乐观锁是什么)
        - [206.你常用的mysql引擎有哪些?各引擎间有什么区别?](#206你常用的mysql引擎有哪些各引擎间有什么区别)
    - [Redis](#redis)
        - [207.Redis宕机怎么解决?](#207redis宕机怎么解决)
        - [208.redis和mecached的区别，以及使用场景](#208redis和mecached的区别以及使用场景)
        - [209.Redis集群方案该怎么做?都有哪些方案?](#209redis集群方案该怎么做都有哪些方案)
        - [210.Redis回收进程是如何工作的](#210redis回收进程是如何工作的)
    - [MongoDB](#mongodb)
        - [211.MongoDB中对多条记录做更新操作命令是什么？](#211mongodb中对多条记录做更新操作命令是什么)
        - [212.MongoDB如何才会拓展到多个shard里？](#212mongodb如何才会拓展到多个shard里)
    - [测试](#测试)
        - [213.编写测试计划的目的是](#213编写测试计划的目的是)
        - [214.对关键词触发模块进行测试](#214对关键词触发模块进行测试)
        - [215.其他常用笔试题目网址汇总](#215其他常用笔试题目网址汇总)
        - [216.测试人员在软件开发过程中的任务是什么](#216测试人员在软件开发过程中的任务是什么)
        - [217.一条软件Bug记录都包含了哪些内容？](#217一条软件bug记录都包含了哪些内容)
        - [218.简述黑盒测试和白盒测试的优缺点](#218简述黑盒测试和白盒测试的优缺点)
        - [219.请列出你所知道的软件测试种类，至少5项](#219请列出你所知道的软件测试种类至少5项)
        - [220.Alpha测试与Beta测试的区别是什么？](#220alpha测试与beta测试的区别是什么)
        - [221.举例说明什么是Bug？一个bug report应包含什么关键字？](#221举例说明什么是bug一个bug-report应包含什么关键字)
    - [数据结构](#数据结构)
        - [222.数组中出现次数超过一半的数字-Python版](#222数组中出现次数超过一半的数字-python版)
        - [223.求100以内的质数](#223求100以内的质数)
        - [224.无重复字符的最长子串-Python实现](#224无重复字符的最长子串-python实现)
        - [225.通过2个5/6升得水壶从池塘得到3升水](#225通过2个56升得水壶从池塘得到3升水)
        - [226.什么是MD5加密，有什么特点？](#226什么是md5加密有什么特点)
        - [227.什么是对称加密和非对称加密](#227什么是对称加密和非对称加密)
        - [228.冒泡排序的思想？](#228冒泡排序的思想)
        - [229.快速排序的思想？](#229快速排序的思想)
        - [230.如何判断单向链表中是否有环？](#230如何判断单向链表中是否有环)
        - [231.你知道哪些排序算法（一般是通过问题考算法）](#231你知道哪些排序算法一般是通过问题考算法)
        - [232.斐波那契数列](#232斐波那契数列)
        - [233.如何翻转一个单链表？](#233如何翻转一个单链表)
        - [234.青蛙跳台阶问题](#234青蛙跳台阶问题)
        - [235.两数之和 Two Sum](#235两数之和-two-sum)
        - [236.搜索旋转排序数组 Search in Rotated Sorted Array](#236搜索旋转排序数组-search-in-rotated-sorted-array)
        - [237.Python实现一个Stack的数据结构](#237python实现一个stack的数据结构)
        - [238.写一个二分查找](#238写一个二分查找)
        - [239.set 用 in 时间复杂度是多少，为什么？](#239set-用-in-时间复杂度是多少为什么)
        - [240.列表中有n个正整数范围在[0，1000]，进行排序；](#240列表中有n个正整数范围在01000进行排序)
        - [241.面向对象编程中有组合和继承的方法实现新的类](#241面向对象编程中有组合和继承的方法实现新的类)
    - [大数据](#大数据)
        - [242.找出1G的文件中高频词](#242找出1g的文件中高频词)
        - [243.一个大约有一万行的文本文件统计高频词](#243一个大约有一万行的文本文件统计高频词)
        - [244.怎么在海量数据中找出重复次数最多的一个？](#244怎么在海量数据中找出重复次数最多的一个)
        - [245.判断数据是否在大量数据中](#245判断数据是否在大量数据中)



<!-- /TOC -->

# Python-Basics
## Working with files
### 1. There is a json file with about 10K lines of data, write a function to read and process the data 
```python
def get_lines():
    with open('file.txt','rb') as f:
        return f.readlines()

if __name__ == '__main__':
    for e in get_lines():
        process(e) # Process every line of data
```
If we want to process a file with a size of 10G, but the memory is only 4G. How should we achieve it by only modifying the get_lines function and other codes remain unchanged? What are the issues that need to be considered?
```python
def get_lines():
    with open('file.txt','rb') as f:
        for i in f:
            yield i
```
It is better to set the number of rows returned each time, otherwise the reading times are too many。
```python
def get_lines():
    l = []
    with open('file.txt','rb') as f:
      data = f.readlines(60000)
    l.append(data)
    yield l
```
Using mmap library
```python
from mmap import mmap


def get_lines(fp):
    with open(fp,"r+") as f:
        m = mmap(f.fileno(), 0)
        tmp = 0
        for i, char in enumerate(m):
            if char==b"\n":
                yield m[tmp:i+1].decode()
                tmp = i+1

if __name__=="__main__":
    for i in get_lines("fp_some_huge_file"):
        print(i)
```
The issues to be considered are: only 4G of memory cannot read 10G files at a time, and it is necessary to read in the data in batches. Record the location of each read data. If the size of the data read in batches each time is too small will spend too much time in the read operation.
https://stackoverflow.com/questions/30294146/python-fastest-way-to-process-large-file

###  2.Fill in the missing code
```python
def print_directory_contents(sPath):
"""
This function receives the name of the folder as an input parameter
Returns the path of the file in this folder
And the path to the files in its containing folder
"""
import os
for s_child in os.listdir(s_path):
    s_child_path = os.path.join(s_path, s_child)
    if os.path.isdir(s_child_path):
        print_directory_contents(s_child_path)
    else:
        print(s_child_path)
```
## Modules and Libraries
### 3.Enter the date， Output the day, month and year？
```python
import datetime
def dayofyear():
    year = input("Enter the year: ")
    month = input("Enter the month: ")
    day = input("Enter the day: ")
    date1 = datetime.date(year=int(year),month=int(month),day=int(day))
    date2 = datetime.date(year=int(year),month=1,day=1)
    return (date1-date2).days+1
```
### 4.write a function to shuffle elements of a sorted list？
Method #1 : Fisher–Yates shuffle Algorithm

This is one of the famous algorithms that is mainly employed to shuffle a sequence of numbers in python. This algorithm just takes the higher index value, and swaps it with current value, this process repeats in a loop till end of the list.
```python
import random
def shuffle_list(alist):
    # Printing original list
    print ("The original list is : " + str(alist))
    # using Fisher–Yates shuffle Algorithm
    # to shuffle a list
    for i in range(len(test_list)-1, 0, -1):
        # Pick a random index from 0 to i
        j = random.randint(0, i + 1)
        # Swap arr[i] with the element at random index
        test_list[i], test_list[j] = test_list[j], test_list[i]
    # Printing shuffled list
    print ("The shuffled list is : " +  str(test_list))
test_list = [1, 4, 5, 6, 3]
shuffle_list(test_list) 
```
Method #2: Using random.shuffle()
```python
import random
def shuffle_list(test_list):
    # Printing original list
    print("The original list is : " + str(test_list))
    # using random.shuffle() to shuffle a list
    random.shuffle(test_list)
    # Printing shuffled list
    print("The shuffled list is : " + str(test_list))

test_list = [1, 4, 5, 6, 3]
shuffle_list(test_list)
```
Method #3 : Using random.sample()
```python 
import random
def shuffle_list(test_list):
    # Printing original list
    print("The original list is : " + str(test_list))
    # using random.sample() to shuffle a list
    res = random.sample(test_list, len(test_list))
    # Printing shuffled list
    print("The shuffled list is : " + str(res))
test_list = [1, 4, 5, 6, 3]
shuffle_list(test_list)

```
## Data types
### 5.Given a dictionary d= {'a':24,'g':52,'i':12,'k':33}; Sort based on values?
```python
def sort_on_values(dict1):
    # x[0] denotes sort by key；
    # x[1]denotes sort by value。
    new_dict= sorted(dict1.items(),key=lambda x:x[1])
    print(new_dict)
d = {'a': 24, 'g': 52, 'i': 12, 'k': 33}
sort_on_values(d)
sorted(d.items(),key=lambda x:x[1])
output = [('i', 12), ('a', 24), ('k', 33), ('g', 52)]

```
### 6. Dictionary Comprehensions
```python
d = {key:value for (key,value) in iterable}
dict_variable = {key:value for (key,value) in dictonary.items()}
```
### 7.Write a function to reverse a given string "aStr"?
```python
def reverse_string(str1):
    return print(str1[::-1])
reverse_string("Mki")
```
### 8. Process the string "k: 1 | k1: 2 | k2: 3 | k3: 4" into a dictionary {k: 1, k1: 2, ...}
Method #1: Using for loop
```python
str1 = "k:1|k1:2|k2:3|k3:4"
def str2dict(str1):
    dict1 = {}
    for items in str1.split('|'):
        key,value = iterms.split(':')
        dict1[key] = value
    return dict1
 ```
Method #2: Using Dictionary comprehensions
```python
str1 = "k:1|k1:2|k2:3|k3:4"
d = {k:int(v) for t in str1.split("|") for k, v in (t.split(":"), )}
```
### 9. Please sort by the age of the elements in alist from largest to smallest
```python
alist = [{'name':'a','age':20},{'name':'b','age':30},{'name':'c','age':25}]
def sort_by_age(list1):
    return print(sorted(list1,key=lambda x:x['age'],reverse=True))
sort_by_age(alist)
```
### 10.What is the output of the following code？
```python
list = ['a','b','c','d','e']
print(list[10:])
```
The code will output []; an empty list, and no IndexError will be generated. As expected, try to get the members of a list with an index that exceeds the number of members. For example, trying to get members of list [10] and later will cause IndexError: "list index out of range". However, when trying to get a slice of the list, the index will not exceed the number of members at the beginning of the indexError, but only returns an empty list. This becomes a particularly disgusting and intractable disease, because no errors are generated during operation, making it difficult to debug.
### 11.Write a list generator， to generate an arithmetic sequence whose common difference is 11
```python
print([x*11 for x in range(10)])
```
### 12. Given two lists, write a function to find out the same elements and different elements from the two lists
```python
list1 = [1,2,3]
list2 = [3,4,5]
set1 = set(list1)
set2 = set(list2)
print(set1 & set2)
print(set1 ^ set2)
```
### 13. Write python code to delete duplicate elements from a list？
```python
l1 = ['b','c','d','c','a','a']
l2 = list(set(l1))
print(l2)
```
Method 1: Using sort() method
```python
l1 = ['b','c','d','c','a','a']
l2 = list(set(l1))
l2.sort(key=l1.index)
print(l2)
```
Method 2:
```python
l1 = ['b','c','d','c','a','a']
l2 = sorted(set(l1),key=l1.index)
print(l2)
```
Meethod 3: Using for loop：
```python
l1 = ['b','c','d','c','a','a']
l2 = []
for i in l1:
    if not i in l2:
        l2.append(i)
print(l2)
```
### 14.Given two lists A，B ,Find elements that are similar and different in list A and list B
```python
A,B Similar elements： print(set(A)&set(B))
A,B different elements:  print(set(A)^set(B))
```
## Enterprise interview questions
### 15.What is the difference between new style class and the classic class in python？
a. In python, all classes that inherit object are new-style classes

b. Python3 only has new-style classes

c. In Python2, the inherited object is a new-style class, the parent class is not a classic class

d. Classic class is basically not used in Python

e.The search order of attributes for multiple inheritance is different. The new type uses breadth-first search, and the old type uses depth-first search.

### 16.What are built-in data types in Python？
a.  int、  long、 float、  complex

b.  str、 list、  tuple

c. dict 、  set

d. Python3 has no long data type，Only has infinite precision int

### 17. How to implement singleton mode in Python? Please write two ways of implementation?
The singleton pattern is a design pattern that restricts the instantiation of a class to one object. It is a way to provide one and only one object of a particular type. It involves only one class to create methods and specify the objects.
Singleton Design Pattern can be understood by a very simple example of Database connectivity. When each object creates a unique Database Connection to the Database, it will highly affect the cost and expenses of the project. So, it is always better to make a single connection rather than making extra irrelevant connections which can be easily done by Singleton Design Pattern.
Method 1:Using decorators
```python
def singleton(cls):
    instances = {}
    def wrapper(*args, **kwargs):
        if cls not in instances:
            instances[cls] = cls(*args, **kwargs)
        return instances[cls]
    return wrapper
    
    
@singleton
class Foo(object):
    pass
foo1 = Foo()
foo2 = Foo()
print(foo1 is foo2)  # True
```
Method 2：Using base class
New is the method that actually creates the instance object, so the new method of the base class is rewritten to ensure that only one instance is generated when the object is created
```python
class Singleton(object):
    def __new__(cls, *args, **kwargs):
        if not hasattr(cls, '_instance'):
            cls._instance = super(Singleton, cls).__new__(cls, *args, **kwargs)
        return cls._instance
    
    
class Foo(Singleton):
    pass

foo1 = Foo()
foo2 = Foo()

print(foo1 is foo2)  # True
```
Method 3: Metaclasses
metaclasses are used to create class objects. When class objects create instance objects, they must call the call method, so when calling call, make sure to always create only one instance, type() is meta class of python

```python
class Singleton(type):
    def __call__(cls, *args, **kwargs):
        if not hasattr(cls, '_instance'):
            cls._instance = super(Singleton, cls).__call__(*args, **kwargs)
        return cls._instance


# Python2
class Foo(object):
    __metaclass__ = Singleton

# Python3
class Foo(metaclass=Singleton):
    pass

foo1 = Foo()
foo2 = Foo()
print(foo1 is foo2)  # True

```
### 18. Write a class with a function to reverse the input. For example; -123 --> -321 
```python
class Solution(object):
    def reverse(self,x):
        if -10<x<10:
            return x
        str_x = str(x)
        if str_x[0] !="-":
            str_x = str_x[::-1]
            x = int(str_x)
        else:
            str_x = str_x[1:][::-1]
            x = int(str_x)
            x = -x
        return x if -2147483648<x<2147483647 else 0
if __name__ == '__main__':
    s = Solution()
    reverse_int = s.reverse(-120)
    print(reverse_int)
```
### 19. Design a function to traverse a directory and grap all the files with the specified extension
Method 1：
```python
import os

def get_files(dir,suffix):
    res = []
    for root,dirs,files in os.walk(dir):
        for filename in files:
            name,suf = os.path.splitext(filename)
            if suf == suffix:
                res.append(os.path.join(root,filename))

    print(res)

get_files("./",'.pyc')
```
Method 2：
```python
import os

def pick(obj):
    if obj.endswith(".pyc"):
        print(obj)
    
def scan_path(ph):
    file_list = os.listdir(ph)
    for obj in file_list:
        if os.path.isfile(obj):
            pick(obj)
        elif os.path.isdir(obj):
            scan_path(obj)
    
if __name__=='__main__':
    path = input('Enter path')
    scan_path(path)
```
Method 3
```python
from glob import iglob


def func(fp, postfix):
    for i in iglob(f"{fp}/**/*{postfix}", recursive=True):
        print(i)

if __name__ == "__main__":
    postfix = ".pyc"
    func("K:\Python_script", postfix)
```
### 20.Calculate the sum of (1-100) using one line of code
```python
count = sum(range(0,101))
print(count)
```
### 21.Write a Python function to delete elements when traversing a list
Iterate over the new list operation and delete the original list operation
Method 1:
```python
def iterate_delete(alist):
    a = [1,2,3,4,5,6,7,8]
    print(id(a))
    print(id(a[:]))
    for i in a[:]:
        if i>5:
            pass
        else:
        a.remove(i)
    print(a)
    print('-----------')
    print(id(a))

```
```python
#filter
a=[1,2,3,4,5,6,7,8]
b = filter(lambda x: x>5,a)
print(list(b))
```
List comprehension
```python
a=[1,2,3,4,5,6,7,8]
b = [i for i in a if i>5]
print(b)
```
Delete in a list reverse order
A list can be traversed in reverse order, even if the following elements are modified, the cordinates of elements that have not been traversed remain unchanged
```python
a=[1,2,3,4,5,6,7,8]
print(id(a))
for i in range(len(a)-1,-1,-1):
    if a[i]>5:
        pass
    else:
        a.remove(a[i])
print(id(a))
print('-----------')
print(a)
```
### 22. String operation problems
Given a string check if it is Pangram or not. A pangram is a sentence containing every letter in the English Alphabet. Lowercase and Uppercase are considered the same. For exmaple, "A QUICK BROWN FOX JUMPS OVER THE LAZY DOG." 
Define and implement a method get_missing_letter, pass in a string and return missing letters of a PANGRAM. The case in the input string  should be ignored, and the return string should be all lowercase characters and sorted alphabetically (please ignore all non-ACSII characters)


**The following example is for explanation, double quotes do not need to be considered:**

(0)Input: "A quick brown for jumps over the lazy dog"

Return ： ""

(1)Input: "A slow yellow fox crawls under the proactive dog" 

Return: "bjkmqz"

(2)Input : "Lions, and tigers, and bears, oh my!"

Return : "cfjkpquvwxz" 

(3)Input : ""

Return ："abcdefghijklmnopqrstuvwxyz"

```python
def get_missing_letter(a):
    s1 = set("abcdefghijklmnopqrstuvwxyz")
    s2 = set(a.lower())
    ret = "".join(sorted(s1-s2))
    return ret
    
print(get_missing_letter("python"))

# other ways to generate letters
# range("a", "z")
# Method 1:
import string
letters = string.ascii_lowercase
# Method 2:
letters = "".join(map(chr, range(ord('a'), ord('z') + 1)))
```

### 23.Mutable and Immutable data types
A mutable object can change its state or contents while immutable objects cannot.
1,Mutable data types include list,dict. Immutable data types include string，number,tuple.

2,When the modification operation is performed, the mutable type passes the address in memory, that is, it directly modify the value in memory, and does not open up new memory。

3, When the immutable type is changed, it does not change the value in the original memory address, but opens up a new memory, copies the value in the original address, and operates on the value in the newly opened memory。

### 24.What is the difference between "is" and "==" in python？
The == operator compares the values of both the operands and checks for value equality. Whereas is operator checks whether both the operands refer to the same object or not.
is： Compares whether the id values of the two objects are equal, that is, whether the two objects are the same instance object. Whether it points to the same memory address

== ： Checks Whether the contents / values of the two objects compared are equal, calls the object's eq() method by default
### 25. Find all odd numbers in a list and construct a new list
```python
a = [1,2,3,4,5,6,7,8,9,10]
res = [ i for i in a if i%2==1]
print(res)
```
### 26. write one line of code to generate 1+2+3+10248
```python
from functools import reduce
#1.Using built-in sum() function 
num = sum([1,2,3,10248])
print(num)
#2.Using reduce() method
num1 = reduce(lambda x,y :x+y,[1,2,3,10248])
print(num1)
```
### 27.Variable scopes in python？（Variable search order)
LEGB order of function scope

1.What is LEGB?

L： local:  Function scope. A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.

E: enclosing Accessible by the outer and the inner function

G: global: A variable created in the main body of the Python code is a global variable and belongs to the global scope. Global variables are available from within any scope, global and local.

B： build-in 

### 28. The string "123" is converted to '123' without using built-in functions such as 'int()'
Method 1： Using 'str' function
```python
def atoi(s):
    num = 0
    for v in s:
        for j in range(10):
            if v == str(j):
                num = num * 10 + j
    return num
```
Method 2： Using 'ord' function
```python
def atoi(s):
    num = 0
    for v in s:
        num = num * 10 + ord(v) - ord('0')
    return num
```
Method 3: Using 'eval' function
```python
def atoi(s):
    num = 0
    for v in s:
        t = "%s * 1" % v
        n = eval(t)
        num = num * 10 + n
    return num
```
Method 4: Using method 2 with reduce() method
```python
from functools import reduce
def atoi(s):
    return reduce(lambda num, v: num * 10 + ord(v) - ord('0'), s, 0)
```
### 29.Given an array of integers
Given an integer array and a target value, find the two numbers in the array that are the target value. You can assume that each input corresponds to only one answer, and the same elements cannot be reused. Example: Given nums = [2,7,11,15], target = 9 because nums [0] + nums [1] = 2 + 7 = 9, so return [0,1]
```python
class Solution:
    def twoSum(self,nums,target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        d = {}
        size = 0
        while size < len(nums):
            if target-nums[size] in d:
                if d[target-nums[size]] <size:
                    return [d[target-nums[size]],size]
                else:
                    d[nums[size]] = size
                size = size +1
solution = Solution()
list = [2,7,11,15]
target = 9
nums = solution.twoSum(list,target)
print(nums)
```

```python

class Solution(object):
    def twoSum(self, nums, target):
        for i in range(len(nums)):
            num = target - nums[i]
            if num in nums[i+1:]:
                return [i, nums.index(num,i+1)]

```
Sort the dictionary in the list：Assume the following list object，alist=[{"name":"a","age":20},{"name":"b","age":30},{"name":"c","age":25}],Sort the elements in alist according to age from largest to smallest alist=[{"name":"a","age":20},{"name":"b","age":30},{"name":"c","age":25}]
```python
alist_sort = sorted(alist,key=lambda e: e.__getitem__('age'),reverse=True)
```

### 30.python code to remove duplicate element from a list
```python
def distFunc1(a):
    """Using a set to remove duplicate elements"""
    a = list(set(a))
    print(a)

def distFunc2(a):
    """ Take the elements from one list and put it in another list, checking if element already exist """
    list = []
    for i in a:
        if i not in list:
            list.append(i)
    #use sort function if you want a sorted list
    list.sort()
    print(list)

def distFunc3(a):
    """Using a dictionary"""
    b = {}
    b = b.fromkeys(a)
    c = list(b.keys())
    print(c)

if __name__ == "__main__":
    a = [1,2,4,2,4,5,7,10,5,5,7,8,9,0,3]
    distFunc1(a)
    distFunc2(a)
    distFunc3(a)
  
```
### 31. Count the 10 most frequent words in a text？
```python
import re

# Method 1:
def test(filepath):
    
    distone = {}

    with open(filepath) as f:
        for line in f:
            line = re.sub("\W+", " ", line)
            lineone = line.split()
            for keyone in lineone:
                if not distone.get(keyone):
                    distone[keyone] = 1
                else:
                    distone[keyone] += 1
    num_ten = sorted(distone.items(), key=lambda x:x[1], reverse=True)[:10]
    num_ten =[x[0] for x in num_ten]
    return num_ten
    
 
# Method 2 
# Using the built-in most_common function from Counter
import re
from collections import Counter


def test2(filepath):
    with open(filepath) as f:
        return list(map(lambda c: c[0], Counter(re.sub("\W+", " ", f.read()).split()).most_common(10)))
```
### 32.Please write a function that meets the following conditions
The input of this function is a list containing only numbers, and the output is a new list, where each element must meet the following conditions:

1、The element is even

2、The element is in the even position in the original list (index is even)

```python
def num_list(num):
    return [i for i in num if i %2 ==0 and num.index(i)%2==0]

num = [0,1,2,3,4,5,6,7,8,9,10]
result = num_list(num)
print(result)
```
### 33.Use a single list generator to generate a new list
The list contains only values that meet the following conditions, the elements are even slices in the original list
```python
def generate_list(list_data):
    res = (x for x in list_data[::2] if x %2 ==0)
    for element in res:
        print(element, end=" ")

list_dat = [1,2,5,8,10,3,18,6,20]
generate_list(list_dat)
# output : 10 18 20 

```
### 34.Generate the following list [1,4,9,16,25,36,49,64,81,100] using one line of code
```python
# List compressions
[x * x for x in range(1,11)]
```
### 35.Write a function that takes the year, month and day as the input and outputs the day of the year？
```python
import datetime

def determine_day():
    y = int(input("Please enter a 4-digit year:"))
    m = int(input("Please enter the month:"))
    d = int(input("Please enter the day"))
    targetDay = datetime.date(y,m,d)
    dayCount = targetDay - datetime.date(targetDay.year -1,12,31)
    return print(f"{targetDay} is the {dayCount.days} day of the year {y}")
if __name__=="__main__":
    determine_day()
```
### 36.Merge two ordered list l1,l2 without using extend function
```python
def loop_merge_sort(l1,l2):
    tmp = []
    while len(l1)>0 and len(l2)>0:
        if l1[0] <l2[0]:
            tmp.append(l1[0])
            del l1[0]
        else:
            tmp.append(l2[0])
            del l2[0]
    while len(l1)>0:
        tmp.append(l1[0])
        del l1[0]
    while len(l2)>0:
        tmp.append(l2[0])
        del l2[0]
    return tmp
```
### 37.Given an array of arbitrary length, implement a function
All odd numbers be in front of even numbers, and arrange the odd numbers in ascending order, and the even numbers in descending order, such as the string '1982376455', become '1355798642'
```python
# Method 1
def func1(l):
    if isinstance(l, str):
        l = [int(i) for i in l]
    l.sort(reverse=True)
    for i in range(len(l)):
        if l[i] % 2 > 0:
            l.insert(0, l.pop(i))
    print(''.join(str(e) for e in l))

# Method 2
def func2(l):
    print("".join(sorted(l, key=lambda x: int(x) % 2 == 0 and 20 - int(x) or int(x))))
```
### 38. Write a function to find the second largest number in an integer array
```python
def find_second_large_num(num_list):
    """
    Find the second largest number in the array
    """
    # Method 1
    # Sort the elements using sorted() built-in function and output the second last element
    tmp_list = sorted(num_list)
    return print("Method 1\nSecond_large_num is :", tmp_list[-2])
    
    # Method 2
    # Set two flags, one to store the maximum number and one to store the next largest number
    #flag2 stores the next-largest value, flag1 stores the maximum value, traverse the array once, first determine whether it is greater than flag1, if it is greater than the value of flag1 , assign to flag2, assign the value of num_list [i] to flag1, otherwise compare whether its  greater than flag2, if it is greater then assign the value of num_list [i] to flag2, otherwise pass
def find_second_largest_num(num_list)
    flag1 = num_list[0]
    flag2 = num_list[0]
    for i in range(1, len(num_list)):
        if num_list[i] > flag1:
            flag2 = flag1
            flag1 = num_list[i]
        elif num_list[i] > flag2:
            two = num_list[i]
    print("Method 2\nSecond_large_num is :", flag2)
    
    # Method 3
    # Using reduce function and the logical (and, or) operators
    # The basic idea is the same as the second method, but there is no need to use if condition。
    from functools import reduce
    num = reduce(lambda ot, x: ot[1] < x and (ot[1], x) or ot[0] < x and (x, ot[1]) or ot, num_list, (0, 0))[0]
    print("Method 3\nSecond_large_num is :", num)
    
    
if __name__ == '__main___':
    num_list = [34, 11, 23, 56, 78, 0, 9, 12, 3, 7, 5]
    find_second_large_num(num_list)
```
### 39.What is the output of the following function？
```python
def multi():
    return [lambda x : i*x for i in range(4)]
print([m(3) for m in multi()])
```
The correct answer is [9,9,9,9], not [0,3,6,9]. This is caused by the behavior of closures in python, which means that the variables in the closure are in an internal function and it is searched when it is called, when the last function is called, the for loop is completed, the value of i is equal 3, so each return value of i is 3, so the final result is [9, 9,9,9]
### 40. Count the number of occurrences of characters in a string
```python
# Method 1
def count_str(str_data):
    """Define a function of frequency of occurance of a character"""
    dict_str = {} 
    for i in str_data:
        dict_str[i] = dict_str.get(i, 0) + 1
    return dict_str
dict_str = count_str("AAABBCCAC")
str_count_data = ""
for k, v in dict_str.items():
    str_count_data += k + str(v)
print(str_count_data)

# Method 2
from collections import Counter

print("".join(map(lambda x: x[0] + str(x[1]), Counter("AAABBCCAC").most_common())))
```
### 41. What are some specific use cases of super() function
Super is used to] return a proxy object that delegates method calls to a parent or sibling class of type. This is useful for accessing inherited methods that have been overridden in a class. The search order is same as that used by getattr() except that the type itself is skipped.
Some common uses are as follows:
Use Case 1: Super can be called upon in a single inheritance, in order to refer to the parent class or multiple classes without explicitly naming them. It’s somewhat of a shortcut, but more importantly, it helps keep your code maintainable for the foreseeable future.
Use Case 2: Super can be called upon in a dynamic execution environment for multiple or collaborative inheritance. This use is considered exclusive to Python, because it’s not possible with languages that only support single inheritance or are statically compiled.
Check the following links for examples on how super() builti-in function is used and exmaples.
https://stackoverflow.com/questions/576169/understanding-python-super-with-init-methods
https://appdividend.com/2019/01/22/python-super-function-example-super-method-tutorial/

#  Advanced Python
## Metaclass
### 42. What is the difference between class instance methods and static methods?
@classmethod: This decorator exists so you can create class methods that are passed the actual class object within the function call, much like self is passed to any other ordinary instance method in a class.

Instance methods: Instance methods are the most common type of methods in Python classes. These are so called because they can access unique data of their instance. If you have two objects each created from a car class, then they each may have different properties. They may have different colors, engine sizes, seats, and so on. Instance methods must have self as a parameter, but you don’t need to pass this in every time. Self is another Python special term. Inside any instance method, you can use self to access any data or methods that may reside in your class. You won’t be able to access them without going through self.

@staticmethod: The @staticmethod decorator is similar to @classmethod in that it can be called from an uninstantiated class object, although in this case there is no cls parameter passed to its method. 

Though classmethod and staticmethod are quite similar, there's a slight difference in usage for both entities: classmethod must have a reference to a class object as the first parameter, whereas staticmethod can have no parameters at all.

Regular methods of  a class automatically takes the class instance as the fisrt argument 
```python
class Date(object):

    def __init__(self, day=0, month=0, year=0):
        self.day = day
        self.month = month
        self.year = year

    @classmethod
    def from_string(cls, date_as_string):
        day, month, year = map(int, date_as_string.split('-'))
        date1 = cls(day, month, year)
        return date1

    @staticmethod
    def is_date_valid(date_as_string):
        day, month, year = map(int, date_as_string.split('-'))
        return day <= 31 and month <= 12 and year <= 3999

date2 = Date.from_string('11-09-2012')
is_date = Date.is_date_valid('11-09-2012')

### 43. Iterate over all attributes of an object and print each attribute name？
```python
class Car:
    def __init__(self,name,loss): # loss [price，Fuel consumption，kilometers]
        self.name = name
        self.loss = loss
    
    def getName(self):
        # Get the name of the car
        return self.name
    
    def getPrice(self):
        # Get the price of the car
        return self.loss[0]
    
    def getLoss(self):
        # Get car wear value
        return self.loss[1] * self.loss[2]

Bmw = Car("BMW",[60,9,500]) # Instantiate a BMW car object
print(getattr(Bmw,"name")) # Use getattr() to pass in the object name, attribute value。
print(dir(Bmw)) # Get all the properties and methods of BMW
```
### 44.Write a class that supports as many operators as possible?
```python
class SampleClass:
    __list = []
    
    def __init__(self):
        print "constructor"
    
    def __del__(self):
        print "destruct"
    
    def __str__(self):
        return "this self-defined array class"

    def __getitem__(self,key):
        return self.__list[key]
    
    def __len__(self):
        return len(self.__list)

    def Add(self,value):
        self.__list.append(value)
    
    def Remove(self,index):
        del self.__list[index]
    
    def DisplayItems(self):
        print "show all items---"
        for item in self.__list:
            print item
    
        
```
### 45.Describe the drawbacks of Cython，Pypy Cpython Numba
Cython
### 46.Please describe the difference and connection between abstract class and interface class
1. An abstract class can have instance methods that implement a default behavior. An Interface can only declare constants and instance methods, but cannot implement default behavior and all methods are implicitly abstract. An interface has all public members and no implementation

2. Interfaces can be inherited, abstract classes cannot

3. Interface definition methods, no implemented code, and abstract classes can implement some methods

4. The basic data type in the interface is static and the abstract class is not

### 47. How to dynamically get and set the attributes of an object in Python？
hasattr() function can be used to determine whether an attribute exist. getattr() is used for getting the attributes while setattr() is used for setting the attributes. An example is shown below:
```python
if hasattr(Parent, 'x'):
    print(getattr(Parent, 'x'))
    setattr(Parent, 'x',3)
print(getattr(Parent,'x'))
```

## Memory management and garbage collection mechanism
### 48.What operations will cause Python memory overflow, how to deal with those causes？
### 49.Regarding Python memory management, which of the following statements is wrong  B

A,Variables do not have to be declared in advance               
B,Variables can be used directly without first being created and assigned
C,Variables do not need to specify types                        
D,You can use del to release resources

### 50.Python's memory management mechanism and tuning methods？

Memory management mechasnism: Reference counting、garbage collection、Memory pool

Reference counting：Reference counting is a very efficient means of memory management. When a Python object is referenced, its reference count increases by 1, When it is no longer referenced by a variable, the count is decremented by 1. When the reference count is equal to 0, the object is deleted. Weak references do not increase the reference count
Garbage collection：

1.Reference counting

Reference counting is also a garbage collection mechanism, and it is also the most intuitive and simplest garbage collection technology. When the reference count of an object in Python drops to 0, it means that there is no reference to the object, and the object becomes garbage to be recycled. For example, a newly created object is assigned to a reference, the object's reference count becomes 1, if the reference is deleted, the object's reference count is 0, then the object can be garbage collected. However, if there is a circular reference, the reference counting mechanism is no longer effective.。

https://foofish.net/python-gc.html

Tuning methods

1.Manual garbage collection

2.Raise the garbage collection threshold

3.Avoid loop references

### 51. What is a memory leak? How to avoid it?

**Memory leak**Refers to a program that fails to free memory that is no longer in use due to negligence or error. Memory leak does not refer to the physical disappearance of memory, but after an application allocates a certain section of memory, due to a design error, the control of the section of memory is lost before the section of memory is released, resulting in a waste of memory。
https://en.wikipedia.org/wiki/Memory_leak

Circular references between objects with `__del __ ()` functions are the main cause of memory leaks. When not using an object, use: del object to delete the reference count of an object to effectively prevent memory leaks.

View the details of objects that cannot be recycled through the Python extension module gc。

You can use sys.getrefcount (obj) to get the reference count of an object, and determine whether a memory leak is based on whether the return value is 0

## Python functions
### 52.What are common list comprehensions？

[expression for variable in list] OR [expression for variable in list if  condition]

### 53.Describe the difference among read、readline、readlines？

read                        Read the entire file

readline                    Read one line

readlines                   Read the entire file into an iterator for us to traverse

### 54.What is a Hash function？

**Hash function** It is a method to create small digital "fingerprints" from any kind of data. The hash function compresses the message or data into a digest, making the amount of data smaller and fixing the format of the data. This function shuffles the data and recreates a fingerprint called hash values, hash codes, hash sums, or hashes. The hash value is usually represented by a string of short random letters and numbers

### 55.Python function overloading mechanism？

Function overloading is mainly to solve two problems.
1。Variable parameter types。
2。Variable number of parameters。

In addition, a basic design principle is that only when the two functions except the parameter type and the number of parameters are the same, then use function overloading, if the functions of the two functions are actually different, then not You should use overloading, and you should use a function with a different name.

Okay, so for case 1, the function is the same, but the parameter type is different, how does Python handle it? The answer is that there is no need to deal with it at all, because Python can accept any type of parameter. If the function of the function is the same, then the different parameter types are likely to be the same code in Python, and there is no need to make two different functions.

So for case 2, the function is the same, but the number of parameters is different, how does Python handle it? As you know, the answer is the default parameters. Set the default parameters for those missing parameters to solve the problem. Because you assume that functions have the same function, those missing parameters are needed after all.

好了，鉴于情况 1 跟 情况 2 都有了解决方案，python 自然就不需要函数重载了。

### 56.Write a function to find the second largest number in an integer array
### 57.Write a decorator function to determine the current time
```python
import datetime


class TimeException(Exception):
    def __init__(self, exception_info):
        super().__init__()
        self.info = exception_info

    def __str__(self):
        return self.info


def timecheck(func):
    def wrapper(*args, **kwargs):
        if datetime.datetime.now().year == 2019:
            func(*args, **kwargs)
        else:
            raise TimeException("Function already expired")

    return wrapper


@timecheck
def test(name):
    print("Hello {}, 2019 Happy".format(name))


if __name__ == "__main__":
    test("backbp")
```
### 58. Write a function to filter items from a list using the built-in filter() function？
```python
list(filter(lambda x: x % 2 == 0, range(10)))
```
### 59. The four principles of writing a function in Python 编写函数的4个原则

1. The function should be as short as possible

2. Function declarations should be reasonable, simple, and easy to use

3. Function parameter design should consider backward compatibility

4.  Single-responsibility functions; Functions should do what they say they do—no more, no less.A function only does one thing, try to ensure the consistency of function statement granularity

### 60. Is the function call parameter passed by value or by reference？

Python parameter passing methods include: positional parameters, default parameters, variable parameters, keyword parameters

Whether the passing of value to a function is by value or by reference depends on the situation:

Immutable parameters are passed by value: immutable objects like integers and strings are passed by copy, because you cannot change the immutable object in place.

Mutable parameters are passed by reference: for example, objects such as lists and dictionaries are passed by reference, which is very similar to passing arrays by pointers in C. Variable objects can be changed inside functions.

### 61.How to set a global variable in function?
Global variables are the one that are defined and declared outside a function and we need to use them inside a function.

Rules of global keyword:
1. If a variable is assigned a value anywhere within the function’s body, it’s assumed to be a local unless explicitly declared as global.
2. Variables that are only referenced inside a function are implicitly global.
3. We Use global keyword to use a global variable inside a function.
4. There is no need to use global keyword outside a function.
```python
def define_global():
    globals() # Return a dictionary containing the current global variables。
    global variable_name # Set a global variable
    return variable-name
```

### 62. Understanding of default parameters ？

The default parameter refers to the case where the default parameter is called when no parameter is passed in when calling the function. When the function parameter is assigned at the same time when calling the function, the incoming parameter will replace the default parameter.
*args and **kwargs allow you to pass multiple arguments or keyword arguments to a function. 

*args is an indefinite length parameter, which can indicate that the input parameter is uncertain, and can be any number。It allows you to pass a varying number of positional arguments. 

** kwargs are keyword parameters. When assigning values, key-value pairs are used. Parameters can be any number of pairs when defining functions. **kwargs works just like *args, but instead of accepting positional arguments it accepts keyword (or named) arguments.

When you are not sure how many parameters will be passed in, you can use two parameters *args and **kwargs.

### 63. How to limit IP access in MYSQL？
GRANT ALL PRIVILEGES ON * . * TO  'ryan'@'IP OF EXTERNAL SERVER'


### 64.Decorators with parameters?

Decorators with fixed-length parameters

```python
def new_func(func):
    def wrappedfun(username, passwd):
        if username == 'root' and passwd == '123456789':
            print('Certified')
            print('Start performing additional functions')
            return func()
       	else:
            print('Incorrect username or password')
            return
    return wrappedfun

@new_func
def origin():
    print('Start executing the function')
origin('root','123456789')
```

Decorators with variable length parameters

```python
def new_func(func):
    def wrappedfun(*parts):
        if parts:
            counts = len(parts)
            print('This system included ', end='')
            for part in parts:
                print(part, ' ',end='')
            print('etc', counts, 'part')
            return func()
        else:
            print('Incorrect username or password')
            return func()
   return wrappedfun

```

### 65. Why function names can be used as parameters?
Everything in Python is an object, the function name is the space of the function in memory, and it is also an object. Because functions are objects we can pass them as arguments to other functions. Functions that can accept other functions as arguments are also called higher-order functions. 
# Python program to illustrate functions can be passed as arguments to other functions  
```python
def shout(text):  
    return text.upper()  
  
def whisper(text):  
    return text.lower()  
  
def greet(func):  
    # storing the function in a variable  
    greeting = func("Hi, I am created by a function passed as an argument.")  
    print(greeting) 
  
greet(shout)  
greet(whisper) 
```
 Output : 
HI, I AM CREATED BY A FUNCTION PASSED AS AN ARGUMENT.
hi, i am created by a function passed as an argument.
### 66. What is the role of the pass statement in Python？

It is used as a dummy place holder whenever a syntactical requirement of a certain programming element is to be fulfilled without assigning any operation. In other words, the pass statement is simply ignored by the Python interpreter and can be seen as a null statement. It is generally used as a dummy statement in a code block, for example in the if or else block.

The pass statement is commonly used in the early stages of program development to form a skeleton of the entire code. Initially, the programmer will create place holders with no operation using pass for various conditional statements, functions, classes etc., and eventually will fill their functionality.

For example:
```python
for num in range(1,6):    
    # using pass in a for loop    
    if num==3:
        pass
    else:
        print ("Num =  {} ".format(num))
```

```python
def implement_later():
    # using pass in a function
    pass

```
### 67. Given the following code, what will be the output of print(c), why?

```python
a = 10
b = 20
c = [a]
a = 15
```
The output will be 10, strings and numbers passes their values

### 68. What are different way of Swaping the values of two variables？

Method 1
```python
a, b = b, a
```

Method 2:
``` python
def swap(a,b):
    print(a,b)
    c = a # create another variable c
    a =b
    b=c
    return print(a,b)
```


### 69. Using map() and reduce() functions in Python？
map() function returns a map object(which is an iterator) of the results after applying the given function to each item of a given iterable (list, tuple etc.)
syntax map(fun, iter)
    un : It is a function to which map passes each element of given iterable.
    iter : It is a iterable which is to be mapped; list, tuple, dictionary, etc.
```python

map(lambda x: x * x, [1, 2, 3, 4])   # Using lambda
# [1, 4, 9, 16]

The reduce() function accepts a function and a sequence and returns a single value calculated as follows:

Initially, the function is called with the first two items from the sequence and the result is returned.
The function is then called again with the result obtained in step 1 and the next value in the sequence. This process keeps repeating until there are items in the sequence.
The syntax of the reduce() function is as follows:

# Syntax: reduce(function, sequence[, initial]) -> value
reduce(lambda x, y: x * y, [1, 2, 3, 4])  # Equals to ((1 * 2) * 3) * 4
# 24
```



### 70.How the callback function communicates?

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
The callback function passes the function pointer (address) as a parameter to another function, treat the entire function as an object, and assign it to the calling function.

A callback takes two parameters: the LocalSolver object that triggers the event and the type of the callback. It is possible to use the same callback method or object for multiple events or multiple LocalSolver instances. The method can be a static function or a method on a class.

### 71. What are the main built-in data types in Python? What is the output of print dir (‘a’)?

built-in data types：boolean，integer，string，list，Tuple，dictionary，set

The output is a string 'a'

### 72.What is the output of map(lambda x:xx，[y for y in range(3)])？

```
[0, 1, 4]
```

### 73. What is the detailed use cases of the following functions hasattr(), getattr(), setattr()？

hasattr(object,name)function: 
hasattr() is an inbuilt utility function in Python whose main task is to check if an object has the given named attribute and return true if present, else false.

Determines whether there is a name attribute or name method in an object, returns a bool value, returns True if there is a name attribute (method), otherwise returns False.
Syntax : hasattr(obj, key)

Parameters :
    obj : The object whose which attribute has to be checked.
    key : Attribute which needs to be checked.

    Returns : Returns True, if attribute is present else returns False.

```python
class Demo(object):
    name = 'demo'
    def run(self):
        return "hello function"
functiondemo = Demo()
res = hasattr(functiondemo, "name") # Check if the class has name attribute，True
res = hasattr(functiondemo, "run") # Check if  the class has run method，True
res = hasattr(functiondemo, "age") # Check if the class has age attribute，False
print(res)
```

getattr(object, name[,default]) function：

getattr() function is used to access the attribute value of an object and also give an option of executing the default value in case of unavailability of the key. This has greater application to check for available keys in web development and many other phases of day-to-day programming.

Syntax : getattr(obj, key, def)

Parameters :
obj : The object whose attributes need to be processed.
key : The attribute of object
def : The default value that need to be printed in case attribute is not found.

Returns :
Object value if value is available, default value in case attribute is not present
and returns AttributeError in case attribute is not present and default value is not
specified.

```python
functiondemo = Demo()
getattr(functiondemo, "name")# Get the value of the name attribute，Print out if it exists --- demo
getattr(functiondemo, "run") # Get run method，print out the memory address of the method if it exists
getattr(functiondemo, "age") # Get non-existent attributes report errors
getattr(functiondemo, "age", 18)# Get non-existent attributes，Returns the default value
```

setattr(object, name, values)function：

setattr() is used to assign the object attribute its value. Apart from ways to assign values to class variables, through constructors and object functions, this method gives you an alternative way to assign value.
setattr() can be used to assign None to any object attribute.
setattr() can be used to initialize a new object attribute.
Syntax : setattr(obj, var, val)

Parameters :
obj : Object whose which attribute is to be assigned.
var : object attribute which has to be assigned.
val : value with which variable is to be assigned.

Returns 
```python
class Demo(object):
    name = "demo"
    def run(self):
        return "hello function"
functiondemo = Demo()
res = hasattr(functiondemo, "age") # Check if age attribute exists，False
print(res)
setattr(functiondemo, "age", 18) # sets the value of age attribute，No return value
res1 = hasattr(functiondemo, "age") # Determine if the attribute exists again，True
```

Comprehensive usecase

```python
class function_demo(object):
    name = "demo"
    def run(self):
        return "hello function"
functiondemo = function_demo()
res = hasattr(functiondemo, "addr") # First determine whether it exists
if res:
    addr = getattr(functiondemo, "addr")
    print(addr)
else:
    addr = getattr(functiondemo, "addr", setattr(functiondemo, "addr", "北京首都"))
    print(addr)
```



### 74.Solve the factorial function using one line of code？

```
reduce(lambda x,y : x*y,range(1,n+1))
```



### 75. What is a lambda function？ What are the benefits of using lambda function？

A lambda function is a small anonymous function. It can take any number of arguments, but can only have one expression.  The lambda keyword is used to create anonymous functions.
Syntax: lambda arguments: expression
This function can have any number of arguments but only one expression, which is evaluated and returned.
One is free to use lambda functions wherever function objects are required.
You need to keep in your knowledge that lambda functions are syntactically restricted to a single expression.
It has various uses in particular fields of programming besides other types of expressions in functions.

The benefits include:
1.lambda function is relatively portable, ready to use, very suitable for the need to complete a function, but this function is only used in this place, even if the name is very random

2.Anonymous function，Generally used to provide functional programming services functions such as filter and map

3.As a callback function, passed to some applications, such as message processing

### 76. What are the termination conditions for recursive functions？
In programming terms a recursive function can be defined as a routine that calls itself directly or indirectly.
The termination condition of recursion is generally defined inside the recursive function. A conditional judgment is made before the recursive call. According to the result of the judgment, choose whether to continue calling itself or return, and return to terminate recursion.

1.Termination conditions: determine whether the number of recursion reaches a certain limit

2.Determine whether the result of the operation reaches a certain range, etc., choose according to the purpose of the design

### 77.What will be the output of the following code? Please explain.

```python
def multipliers():
    return [lambda x: i *x for i in range(4)]
	print([m(2) for m in multipliers()])

```

The output of the above code is [6,6,6,6], not [0,2,4,6]

How do you modify the multipliers() function above to return the desired result？

The reason for the above problem is the late binding of Python closures. This means that when the internal function is called, the value of the parameter is searched in the closure. Therefore, when any function returned by multipliers () is called, the value of i will be searched in the nearby range. At that time, regardless of whether the returned function is called, the for loop has completed and i is given the final value of 3.

# Method 1:
```python
def multipliers():
    for i in range(4):
        yield lambda x: i *x
```

# Method 2:
```python
def multipliers():
    return [lambda x,i = i: i*x for i in range(4)]

```

### 78. What is a lambda function? What are the benefits? Write an anonymous function to find the sum of two numbers

The lambda function is an anonymous function. This function is named after omitting the standard step of declaring a function with def

```python
add = lambda x, y : x + y
 
print(add(10, 20))

```

##  Python Design Patterns
### 79. Understanding of design patterns, briefly describe the design patterns you understand？

Design pattern is summarized, optimized, and reusable solution to some programming problems we often encounter. A design pattern does not directly affect our code like a class or a library. On the contrary, the design pattern is more advanced. It is a method template that must be implemented in a specific situation.
Common design patterns are the factory pattern and singleton pattern
### 80.Write one singleton class

Singleton Method is a type of Creational Design pattern and is one of the simplest design pattern available to us. It is a way to provide one and only one object of a particular type. It involves only one class to create methods and specify the objects.
Singleton Design Pattern can be understood by a very simple example of Database connectivity. When each object creates a unique Database Connection to the Database, it will highly affect the cost and expenses of the project. So, it is always better to make a single connection rather than making extra irrelevant connections which can be easily done by Singleton Design Pattern.
```python
#python2
class A(object):
    __instance = None
    def __new__(cls,*args,**kwargs):
        if cls.__instance is None:
            cls.__instance = objecet.__new__(cls)
            return cls.__instance
        else:
            return cls.__instance
```
### 81.What are some common usecases of singleton design pattern？
Singleton pattern application scenarios are generally found under the following conditions:
In the case of resource sharing, avoid performance or loss due to resource operations, such as log files and application configuration.
In the case of controlling resources, it is convenient to communicate with each other. Such as thread pool, etc. 
1. website counter 
2. application configuration 
3. multi-thread pool 
4. database configuration, database connection pool 
5. application log  etc
### 82.用一行代码生成[1,4,9,16,25,36,49,64,81,100]
```python
print([x*x for x in range(1, 11)])
```
### 83.对装饰器的理解，并写出一个计时器记录方法执行性能���装饰器？
装饰器本质上是一个callable object ，它可以让其他函数在不需要做任何代码变动的前提下增加额外功能，装饰器的返回值也是一个函数对象。

```python
import time
from functools import wraps

def timeit(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        start = time.clock()
        ret = func(*args, **kwargs)
        end = time.clock()
        print('used:',end-start)
        return ret
    
    return wrapper
@timeit
def foo():
    print('in foo()'foo())
```
### 84.解释以下什么是闭包？
在函数内部再定义一个函数，并且这个函数用到了外边函数的变量，那么将这个函数以及用到的一些变量称之为闭包。

### 85.函数装饰器有什么作用？
装饰器本质上是一个callable object，它可以在让其他函数在不需要做任何代码的变动的前提下增加额外的功能。装饰器的返回值也是一个函数的对象，它经常用于有切面需求的场景。比如：插入日志，性能测试，事务处理，缓存。权限的校验等场景，有了装饰器就可以抽离出大量的与函数功能本身无关的雷同代码并发并继续使用。
详细参考：https://manjusaka.itscoder.com/2018/02/23/something-about-decorator/

### 86.生成器，迭代器的区别？
迭代器是遵循迭代协议的对象。用户可以使用 iter() 以从任何序列得到迭代器（如 list, tuple, dictionary, set 等）。另一个方法则是创建一个另一种形式的迭代器 —— generator 。要获取下一个元素，则使用成员函数 next()（Python 2）或函数 next() function （Python 3） 。当没有元素时，则引发 StopIteration 此例外。若要实现自己的迭代器，则只要实现 next()（Python 2）或 `__next__`()（ Python 3）

生成器（Generator），只是在需要返回数据的时候使用yield语句。每次next()被调用时，生成器会返回它脱离的位置（它记忆语句最后一次执行的位置和所有的数据值）


区别： 生成器能做到迭代器能做的所有事，而且因为自动创建iter()和next()方法，生成器显得特别简洁，而且生成器也是高效的，使用生成器表达式取代列表解析可以同时节省内存。除了创建和保存程序状态的自动方法，当发生器终结时，还会自动抛出StopIteration异常。

官方介绍：https://docs.python.org/3/tutorial/classes.html#iterators
### 87.X是什么类型?
    X= (i for i in range(10))
    X是 generator类型
### 88.请用一行代码 实现将1-N 的整数列表以3为单位分组
```python
N =100
print ([[x for x in range(1,100)] [i:i+3] for i in range(0,100,3)])
```
### 89.Python中yield的用法?
yield就是保存当前程序执行状态。你用for循环的时候，每次取一个元素的时候就会计算一次。用yield的函数叫generator,和iterator一样，它的好处是不用一次计算所有元素，而是用一次算一次，可以节省很多空间，generator每次计算需要上一次计算结果，所以用yield,否则一return，上次计算结果就没了
## 面向对象
### 90.Python中的可变对象和不可变对象？

不可变对象，该对象所指向的内存中的值不能被改变。当改变某个变量时候，由于其所指的值不能被改变，相当于把原来的值复制一份后再改变，这会开辟一个新的地址，变量再指向这个新的地址。

可变对象，该对象所指向的内存中的值可以被改变。变量（准确的说是引用）改变后，实际上其所指的值直接发生改变，并没有发生复制行为，也没有开辟出新的地址，通俗点说就是原地改变。

Pyhton中，数值类型(int 和float)，字符串str、元祖tuple都是不可变类型。而列表list、字典dict、集合set是可变类型

### 91.Python的魔法方法

魔法方法就是可以给你的类增加魔力的特殊方法，如果你的对象实现（重载）了这些方法中的某一个，那么这个方法就会在特殊的情况下被Python所调用，你可以定义自己想要的行为，而这一切都是自动发生的，它们经常是两个下划线包围来命名的（比如`__init___`,`__len__`),Python的魔法方法是非常强大的所以了解其使用方法也变得尤为重要!

`__init__`构造器，当一个实例被创建的时候初始化的方法，但是它并不是实例化调用的第一个方法。

`__new__`才是实例化对象调用的第一个方法，它只取下cls参数，并把其他参数传给`__init___`.

`___new__`很少使用，但是也有它适合的场景，尤其是当类继承自一个像元祖或者字符串这样不经常改变的类型的时候。

`__call__`让一个类的实例像函数一样被调用

`__getitem__`定义获取容器中指定元素的行为，相当于self[key]

`__getattr__`定义当用户试图访问一个不存在属性的时候的行为。

`__setattr__`定义当一个属性被设置的时候的行为

`__getattribute___`定义当一个属性被访问的时候的行为

### 92.面向对象中怎么实现只读属性?

将对象私有化，通过共有方法提供一个读取数据的接口

```python
class person:
    def __init__(self, x):
        self.__age = 10
    def age(self):
        return self.__age
t = person(22)
# t.__age =100
print(t.age())
```

最好的方法

```python
class MyCls(object):
    __weight = 50
    
    @property
    def weight(self):
        return self.__weight
   
```

### 93.谈谈你对面向对象的理解？

面向对象是相当于面向过程而言的，面向过程语言是一种基于功能分析的，以算法为中心的程序设计方法，而面向对象是一种基于结构分析的，以数据为中心的程序设计思想。在面向对象语言中有一个很重要的东西，叫做类。面向对象有三大特性：封装、继承、多态。

## 正则表达式
### 94.请写出一段代码用正则匹配出ip？

### 95.a = “abbbccc”，用正则匹配为abccc,不管有多少b，就出现一次？
    思路：不管有多少个b替换成一个

    re.sub(r'b+', 'b', a)
### 96.Python字符串查找和替换？
    a、str.find()：正序字符串查找函数
    函数原型：
    str.find(substr [,pos_start [,pos_end ] ] )
    返回str中第一次出现的substr的第一个字母的标号，如果str中没有substr则返回-1，也就是说从左边算起的第一次出现的substr的首字母标号。

    参数说明：
    str：代表原字符串
    substr：代表要查找的字符串
    pos_start：代表查找的开始位置，默认是从下标0开始查找
    pos_end：代表查找的结束位置

    例子：
    'aabbcc.find('bb')' # 2

    b、str.index()：正序字符串查找函数
    index()函数类似于find()函数，在Python中也是在字符串中查找子串第一次出现的位置，跟find()不同的是，未找到则抛出异常。

    函数原型：
    str.index(substr [, pos_start, [ pos_end ] ] )

    参数说明：
    str：代表原字符串
    substr：代表要查找的字符串
    pos_start：代表查找的开始位置，默认是从下标0开始查找
    pos_end：代表查找的结束位置

    例子：
    'acdd l1 23'.index(' ') # 4

    c、str.rfind()：倒序字符串查找函数

    函数原型：
    str.rfind( substr [, pos_start [,pos_ end ] ])
    返回str中最后出现的substr的第一个字母的标号，如果str中没有substr则返回-1，也就是说从右边算起的第一次出现的substr的首字母标号。

    参数说明：
    str：代表原字符串
    substr：代表要查找的字符串
    pos_start：代表查找的开始位置，默认是从下标0开始查找
    pos_end：代表查找的结束位置

    例子：
    'adsfddf'.rfind('d') # 5

    d、str.rindex()：倒序字符串查找函数
    rindex()函数类似于rfind()函数，在Python中也是在字符串中倒序查找子串最后一次出现的位置，跟rfind()不同的是，未找到则抛出异常。

    函数原型：
    str.rindex(substr [, pos_start, [ pos_end ] ] )

    参数说明：
    str：代表原字符串
    substr：代表要查找的字符串
    pos_start：代表查找的开始位置，默认是从下标0开始查找
    pos_end：代表查找的结束位置

    例子：
     'adsfddf'.rindex('d') # 5

    e、使用re模块进行查找和替换：
函数 | 说明
---|---
re.match(pat, s) | 只从字符串s的头开始匹配，比如(‘123’, ‘12345’)匹配上了，而(‘123’,’01234’)就是没有匹配上，没有匹配上返回None，匹配上返回matchobject
re.search(pat, s) | 从字符串s的任意位置都进行匹配，比如(‘123’,’01234’)就是匹配上了，只要s只能存在符合pat的连续字符串就算匹配上了，没有匹配上返回None，匹配上返回matchobject
re.sub(pat,newpat,s) | re.sub(pat,newpat,s)	对字符串中s的包含的所有符合pat的连续字符串进行替换，如果newpat为str,那么就是替换为newpat,如果newpat是函数，那么就按照函数返回值替换。sub函数两个有默认值的参数分别是count表示最多只处理前几个匹配的字符串，默认为0表示全部处理；最后一个是flags，默认为0

    f、使用replace()进行替换：
    基本用法：对象.replace(rgExp,replaceText,max)

    其中，rgExp和replaceText是必须要有的，max是可选的参数，可以不加。
    rgExp是指正则表达式模式或可用标志的正则表达式对象，也可以是 String 对象或文字；
    replaceText是一个String 对象或字符串文字；
    max是一个数字。
    对于一个对象，在对象的每个rgExp都替换成replaceText，从左到右最多max次。

    s1='hello world'
    s1.replace('world','liming')

### 97.用Python匹配HTML tag的时候，<.*> 和 <.*?> 有什么区别
    第一个代表贪心匹配，第二个代表非贪心；
    ?在一般正则表达式里的语法是指的"零次或一次匹配左边的字符或表达式"相当于{0,1}
    而当?后缀于*,+,?,{n},{n,},{n,m}之后，则代表非贪心匹配模式，也就是说，尽可能少的匹配左边的字符或表达式，这里是尽可能少的匹配.(任意字符)

    所以：第一种写法是，尽可能多的匹配，就是匹配到的字符串尽量长，第二中写法是尽可能少的匹配，就是匹配到的字符串尽量短。
    比如<tag>tag>tag>end，第一个会匹配<tag>tag>tag>,第二个会匹配<tag>。
### 98.正则表达式贪婪与非贪婪模式的区别？
    贪婪模式：
    定义：正则表达式去匹配时，会尽量多的匹配符合条件的内容
    标识符：+，?，*，{n}，{n,}，{n,m}
    匹配时，如果遇到上述标识符，代表是贪婪匹配，会尽可能多的去匹配内容

    非贪婪模式：
    定义：正则表达式去匹配时，会尽量少的匹配符合条件的内容 也就是说，一旦发现匹配符合要求，立马就匹配成功，而不会继续匹配下去(除非有g，开启下一组匹配)
    标识符：+?，??，*?，{n}?，{n,}?，{n,m}?
    可以看到，非贪婪模式的标识符很有规律，就是贪婪模式的标识符后面加上一个?

    参考文章：https://dailc.github.io/2017/07/06/regularExpressionGreedyAndLazy.html

### 99.写出开头匹配字母和下划线，末尾是数字的正则表达式？
    s1='_aai0efe00'
    res=re.findall('^[a-zA-Z_]?[a-zA-Z0-9_]{1,}\d$',s1)
    print(res)

### 100.正则表达式操作
### 101.请匹配出变量A 中的json字符串。
### 102.怎么过滤评论中的表情？
    思路：主要是匹配表情包的范围，将表情包的范围用空替换掉
```
import re
pattern = re.compile(u'[\uD800-\uDBFF][\uDC00-\uDFFF]')
pattern.sub('',text)

```
### 103.简述Python里面search和match的区别
    match()函数只检测字符串开头位置是否匹配，匹配成功才会返回结果，否则返回None；
    search()函数会在整个字符串内查找模式匹配,只到找到第一个匹配然后返回一个包含匹配信息的对象,该对象可以通过调用group()方法得到匹配的字符串,如果字符串没有匹配，则返回None。

### 104.请写出匹配ip的Python正则表达式
### 105.Python里match与search的区别？
    见103题

## 系统编程
### 106.进程总结
进程：程序运行在操作系统上的一个实例，就称之为进程。进程需要相应的系统资源：内存、时间片、pid。
创建进程：
首先要导入multiprocessing中的Process：
创建一个Process对象;
创建Process对象时，可以传递参数;
```python
p = Process(target=XXX,args=(tuple,),kwargs={key:value})
target = XXX 指定的任务函数，不用加(),
args=(tuple,)kwargs={key:value}给任务函数传递的参数
```
使用start()启动进程
结束进程
给子进程指定函数传递参数Demo
```python
import os
from mulitprocessing import Process
import time

def pro_func(name,age,**kwargs):
    for i in range(5):
        print("子进程正在运行中，name=%s,age=%d,pid=%d"%(name,age,os.getpid()))
        print(kwargs)
        time.sleep(0.2)
if __name__ =="__main__":
    #创建Process对象
    p = Process(target=pro_func,args=('小明',18),kwargs={'m':20})
    #启动进程
    p.start()
    time.sleep(1)
    #1秒钟之后，立刻结束子进程
    p.terminate()
    p.join()
```
注意：进程间不共享全局变量

进程之间的通信-Queue

在初始化Queue()对象时（例如q=Queue(),若在括号中没有指定最大可接受的消息数量，获数量为负值时，那么就代表可接受的消息数量没有上限一直到内存尽头）

Queue.qsize():返回当前队列包含的消息数量

Queue.empty():如果队列为空，返回True，反之False

Queue.full():如果队列满了，返回True,反之False

Queue.get([block[,timeout]]):获取队列中的一条消息，然后将其从队列中移除，

block默认值为True。

如果block使用默认值，且没有设置timeout（单位秒),消息队列如果为空，此时程序将被阻塞（停在读中状态），直到消息队列读到消息为止，如果设置了timeout，则会等待timeout秒，若还没读取到任何消息，则抛出“Queue.Empty"异常：

Queue.get_nowait()相当于Queue.get(False)

Queue.put(item,[block[,timeout]]):将item消息写入队列，block默认值为True;
如果block使用默认值，且没有设置timeout（单位秒），消息队列如果已经没有空间可写入，此时程序将被阻塞（停在写入状态），直到从消息队列腾出空间为止，如果设置了timeout，则会等待timeout秒，若还没空间，则抛出”Queue.Full"异常
如果block值为False，消息队列如果没有空间可写入，则会立刻抛出"Queue.Full"异常;
Queue.put_nowait(item):相当Queue.put(item,False)

进程间通信Demo:
```python
from multiprocessing import Process.Queue
import os,time,random
#写数据进程执行的代码：
def write(q):
    for value in ['A','B','C']:
        print("Put %s to queue...",%value)
        q.put(value)
        time.sleep(random.random())
#读数据进程执行的代码
def read(q):
    while True:
        if not q.empty():
            value = q.get(True)
            print("Get %s from queue.",%value)
            time.sleep(random.random())
        else:
            break
if __name__=='__main__':
    #父进程创建Queue，并传给各个子进程
    q = Queue()
    pw = Process(target=write,args=(q,))
    pr = Process(target=read,args=(q,))
    #启动子进程pw ，写入：
    pw.start()
    #等待pw结束
    pw.join()
    #启动子进程pr，读取：
    pr.start()
    pr.join()
    #pr 进程里是死循环，无法等待其结束，只能强行终止:
    print('')
    print('所有数据都写入并且读完')
```
    进程池Pool
```python
#coding:utf-8
from multiprocessing import Pool
import os,time,random

def worker(msg):
    t_start = time.time()
    print("%s 开始执行，进程号为%d"%(msg,os.getpid()))
    # random.random()随机生成0-1之间的浮点数
    time.sleep(random.random()*2)
    t_stop = time.time()
    print(msg,"执行完毕，耗时%0.2f”%（t_stop-t_start))

po = Pool(3)#定义一个进程池，最大进程数3
for i in range(0,10):
    po.apply_async(worker,(i,))
print("---start----")
po.close()
po.join()
print("----end----")
```
进程池中使用Queue

如果要使用Pool创建进程，就需要使用multiprocessing.Manager()中的Queue(),而不是multiprocessing.Queue(),否则会得到如下的错误信息：

RuntimeError： Queue objects should only be shared between processs through inheritance
```python
from multiprocessing import Manager,Pool
import os,time,random
def reader(q):
    print("reader 启动(%s),父进程为（%s)"%(os.getpid(),os.getpid()))
    for i in range(q.qsize()):
        print("reader 从Queue获取到消息:%s"%q.get(True))

def writer(q):
    print("writer 启动（%s),父进程为(%s)"%(os.getpid(),os.getpid()))
    for i ini "itcast":
        q.put(i)
if __name__ == "__main__":
    print("(%s)start"%os.getpid())
    q = Manager().Queue()#使用Manager中的Queue
    po = Pool()
    po.apply_async(wrtier,(q,))
    time.sleep(1)
    po.apply_async(reader,(q,))
    po.close()
    po.join()
    print("(%s)End"%os.getpid())
```
### 107.谈谈你对多进程，多线程，以及协程的理解，项目是否用？
这个问题被问的概念相当之大，
进程：一个运行的程序（代码）就是一个进程，没有运行的代码叫程序，进程是系统资源分配的最小单位，进程拥有自己独立的内存空间，所有进程间数据不共享，开销大。

线程: cpu调度执行的最小单位，也叫执行路径，不能独立存在，依赖进程存在，一个进程至少有一个线程，叫主线程，而多个线程共享内存（数据共享，共享全局变量),从而极大地提高了程序的运行效率。

协程: 是一种用户态的轻量级线程，协程的调度完全由用户控制。协程拥有自己的寄存器上下文和栈。协程调度时，将寄存器上下文和栈保存到其他地方，在切回来的时候，恢复先前保存的寄存器上下文和栈，直接操中栈则基本没有内核切换的开销，可以不加锁的访问全局变量，所以上下文的切换非常快。

### 108.Python异步使用场景有那些？
异步的使用场景:

1、 不涉及共享资源，获对共享资源只读，即非互斥操作

2、 没有时序上的严格关系

3、 不需要原子操作，或可以通过其他方式控制原子性

4、 常用于IO操作等耗时操作，因为比较影响客户体验和使用性能

5、 不影响主线程逻辑

### 109.多线程共同操作同一个数据互斥锁同步？
```python
import threading
import time
class MyThread(threading.Thread):
    def run(self):
        global num
        time.sleep(1)
    
        if mutex.acquire(1):
            num +=1
            msg = self.name + 'set num to ' +str(num)
            print msg
            mutex.release()
num = 0
mutex = threading.Lock()
def test():
    for i in range(5):
        t = MyThread()
        t.start()
if __name__=="__main__":
    test()
```
### 110.什么是多线程竞争？
线程是非独立的，同一个进程里线程是数据共享的，当各个线程访问数据资源时会出现竞争状态即：数据几乎同步会被多个线程占用，造成数据混乱，即所谓的线程不安全

那么怎么解决多线程竞争问题？---锁

锁的好处： 确保了某段关键代码（共享数据资源）只能由一个线程从头到尾完整地执行能解决多线程资源竞争下的原子操作问题。

锁的坏处： 阻止了多线程并发执行，包含锁的某段代码实际上只能以单线程模式执行，效率就大大地下降了

锁的致命问题: 死锁
### 111.请介绍一下Python的线程同步？
 一、 setDaemon(False)
当一个进程启动之后，会默认产生一个主线程，因为线程是程序执行的最小单位，当设置多线程时，主线程会创建多个子线程，在Python中，默认情况下就是setDaemon(False),主线程执行完自己的任务以后，就退出了，此时子线程会继续执行自己的任务，直到自己的任务结束。

例子
```python
import threading 
import time

def thread():
    time.sleep(2)
    print('---子线程结束---')

def main():
    t1 = threading.Thread(target=thread)
    t1.start()
    print('---主线程--结束')

if __name__ =='__main__':
    main()
#执行结果
---主线程--结束
---子线程结束---
```
二、 setDaemon（True)
当我们使用setDaemon(True)时，这是子线程为守护线程，主线程一旦执行结束，则全部子线程被强制终止

例子
```python
import threading
import time
def thread():
    time.sleep(2)
    print(’---子线程结束---')
def main():
    t1 = threading.Thread(target=thread)
    t1.setDaemon(True)#设置子线程守护主线程
    t1.start()
    print('---主线程结束---')

if __name__ =='__main__':
    main()
#执行结果
---主线程结束--- #只有主线程结束，子线程来不及执行就被强制结束
```
三、 join（线程同步)
join 所完成的工作就是线程同步，即主线程任务结束以后，进入堵塞状态，一直等待所有的子线程结束以后，主线程再终止。

当设置守护线程时，含义是主线程对于子线程等待timeout的时间将会杀死该子线程，最后退出程序，所以说，如果有10个子线程，全部的等待时间就是每个timeout的累加和，简单的来说，就是给每个子线程一个timeou的时间，让他去执行，时间一到，不管任务有没有完成，直接杀死。

没有设置守护线程时，主线程将会等待timeout的累加和这样的一段时间，时间一到，主线程结束，但是并没有杀死子线程，子线程依然可以继续执行，直到子线程全部结束，程序退出。

例子
```python
import threading
import time

def thread():
    time.sleep(2)
    print('---子线程结束---')

def main():
    t1 = threading.Thread(target=thread)
    t1.setDaemon(True)
    t1.start()
    t1.join(timeout=1)#1 线程同步，主线程堵塞1s 然后主线程结束，子线程继续执行
                        #2 如果不设置timeout参数就等子线程结束主线程再结束
                        #3 如果设置了setDaemon=True和timeout=1主线程等待1s后会强制杀死子线程，然后主线程结束
    print('---主线程结束---')

if __name__=='__main___':
    main()
```
### 112.解释以下什么是锁，有哪几种锁？
锁(Lock)是python提供的对线程控制的对象。有互斥锁，可重入锁，死锁。

### 113.什么是死锁？
若干子线程在系统资源竞争时，都在等待对方对某部分资源解除占用状态，结果是谁也不愿先解锁，互相干等着，程序无法执行下去，这就是死锁。

GIL锁 全局解释器锁

作用： 限制多线程同时执行，保证同一时间只有一个线程执行，所以cython里的多线程其实是伪多线程！

所以python里常常使用协程技术来代替多线程，协程是一种更轻量级的线程。

进程和线程的切换时由系统决定，而协程由我们程序员自己决定，而模块gevent下切换是遇到了耗时操作时才会切换

三者的关系：进程里有线程，线程里有协程。
### 114.多线程交互访问数据，如果访问到了就不访问了？
怎么避免重读？

创建一个已访问数据列表，用于存储已经访问过的数据，并加上互斥锁，在多线程访问数据的时候先查看数据是否在已访问的列表中，若已存在就直接跳过。

### 115.什么是线程安全，什么是互斥锁？
每个对象都对应于一个可称为’互斥锁‘的标记，这个标记用来保证在任一时刻，只能有一个线程访问该对象。

同一进程中的多线程之间是共享系统资源的，多个线程同时对一个对象进行操作，一个线程操作尚未结束，另一线程已经对其进行操作，导致最终结果出现错误，此时需要对被操作对象添加互斥锁，保证每个线程对该对象的操作都得到正确的结果。

### 116.说说下面几个概念：同步，异步，阻塞，非阻塞？
同步： 多个任务之间有先后顺序执行，一个执行完下个才能执行。

异步： 多个任务之间没有先后顺序，可以同时执行，有时候一个任务可能要在必要的时候获取另一个同时执行的任务的结果，这个就叫回调！

阻塞： 如果卡住了调用者，调用者不能继续往下执行，就是说调用者阻塞了。

非阻塞： 如果不会卡住，可以继续执行，就是说非阻塞的。

同步异步相对于多任务而言，阻塞非阻塞相对于代码执行而言。

### 117.什么是僵尸进程和孤儿进程？怎么避免僵尸进程？
孤儿进程： 父进程退出，子进程还在运行的这些子进程都是孤儿进程，孤儿进程将被init 进程（进程号为1）所收养，并由init 进程对他们完成状态收集工作。

僵尸进程： 进程使用fork 创建子进程，如果子进程退出，而父进程并没有调用wait 获waitpid 获取子进程的状态信息，那么子进程的进程描述符仍然保存在系统中的这些进程是僵尸进程。

避免僵尸进程的方法：

1.fork 两次用孙子进程去完成子进程的任务

2.用wait()函数使父进程阻塞

3.使用信号量，在signal handler 中调用waitpid,这样父进程不用阻塞
###  118.python中进程与线程的使用场景？
多进程适合在CPU密集操作（cpu操作指令比较多，如位多的的浮点运算）。

多线程适合在IO密性型操作（读写数据操作比多的的，比如爬虫）

###  119.线程是并发还是并行，进程是并发还是并行？
线程是并发，进程是并行;

进程之间互相独立，是系统分配资源的最小单位，同一个线程中的所有线程共享资源。

### 120.并行(parallel)和并发（concurrency)?
并行： 同一时刻多个任务同时在运行

不会在同一时刻同时运行，存在交替执行的情况。

实现并行的库有： multiprocessing

实现并发的库有:  threading

程序需要执行较多的读写、请求和回复任务的需要大量的IO操作，IO密集型操作使用并发更好。

CPU运算量大的程序，使用并行会更好
### 121.IO密集型和CPU密集型区别？
IO密集型： 系统运行，大部分的状况是CPU在等 I/O（硬盘/内存）的读/写

CPU密集型： 大部分时间用来做计算，逻辑判断等CPU动作的程序称之CPU密集型。
### 122.python asyncio的原理？
asyncio这个库就是使用python的yield这个可以打断保存当前函数的上下文的机制， 封装好了selector 摆脱掉了复杂的回调关系

## 网络编程
### 123.怎么实现强行关闭客户端和服务器之间的连接?
### 124.简述TCP和UDP的区别以及优缺点?
### 125.简述浏览器通过WSGI请求动态资源的过程?
浏览器发送的请求被Nginx监听到，Nginx根据请求的URL的PATH或者后缀把请求静态资源的分发到静态资源的目录，别的请求根据配置好的转发到相应端口。
实现了WSGI的程序会监听某个端口，监听到Nginx转发过来的请求接收后(一般用socket的recv来接收HTTP的报文)以后把请求的报文封装成`environ`的字典对象，然后再提供一个`start_response`的方法。把这两个对象当成参数传入某个方法比如`wsgi_app(environ, start_response)`或者实现了`__call__(self, environ, start_response)`方法的某个实例。这个实例再调用`start_response`返回给实现了WSGI的中间件，再由中间件返回给Nginx。
### 126.描述用浏览器访问www.baidu.com的过程
### 127.Post和Get请求的区别?
### 128.cookie 和session 的区别？
### 129.列出你知道的HTTP协议的状态码，说出表示什么意思？
### 130.请简单说一下三次握手和四次挥手？
### 131.说一下什么是tcp的2MSL？
### 132.为什么客户端在TIME-WAIT状态必须等待2MSL的时间？
### 133.说说HTTP和HTTPS区别？
### 134.谈一下HTTP协议以及协议头部中表示数据类型的字段？
### 135.HTTP请求方法都有什么？
### 136.使用Socket套接字需要传入哪些参数 ？
### 137.HTTP常见请求头？
### 138.七层模型？
### 139.url的形式？

# Web
## Flask
### 140.对Flask蓝图(Blueprint)的理解？
蓝图的定义

蓝图 /Blueprint 是Flask应用程序组件化的方法，可以在一个应用内或跨越多个项目共用蓝图。使用蓝图可以极大简化大型应用的开发难度，也为Flask扩展提供了一种在应用中注册服务的集中式机制。

蓝图的应用场景：

把一个应用分解为一个蓝图的集合。这对大型应用是理想的。一个项目可以实例化一个应用对象，初始化几个扩展，并注册一集合的蓝图。

以URL前缀和/或子域名，在应用上注册一个蓝图。URL前缀/子域名中的参数即成为这个蓝图下的所有视图函数的共同的视图参数（默认情况下）
在一个应用中用不同的URL规则多次注册一个蓝图。

通过蓝图提供模板过滤器、静态文件、模板和其他功能。一个蓝图不一定要实现应用或视图函数。

初始化一个Flask扩展时，在这些情况中注册一个蓝图。

蓝图的缺点：

不能在应用创建后撤销注册一个蓝图而不销毁整个应用对象。

使用蓝图的三个步骤

1.创建一个蓝图对象
```python
blue = Blueprint("blue",__name__)
```
2.在这个蓝图对象上进行操作，例如注册路由、指定静态文件夹、注册模板过滤器...
```python
@blue.route('/')
def blue_index():
    return "Welcome to my blueprint"
```
3.在应用对象上注册这个蓝图对象
```python
app.register_blueprint(blue,url_prefix="/blue")
```

### 141.Flask 和 Django 路由映射的区别？
  在django中，路由是浏览器访问服务器时，先访问的项目中的url，再由项目中的url找到应用中url，这些url是放在一个列表里，遵从从前往后匹配的规则。在flask中，路由是通过装饰器给每个视图函数提供的，而且根据请求方式的不同可以一个url用于不同的作用。

## Django
### 142.什么是wsgi,uwsgi,uWSGI?
WSGI:

web服务器网关接口，是一套协议。用于接收用户请求并将请求进行初次封装，然后将请求交给web框架。

实现wsgi协议的模块：wsgiref,本质上就是编写一socket服务端，用于接收用户请求（django)

werkzeug,本质上就是编写一个socket服务端，用于接收用户请求(flask)

uwsgi:

与WSGI一样是一种通信协议，它是uWSGI服务器的独占协议，用于定义传输信息的类型。
uWSGI:

是一个web服务器，实现了WSGI的协议，uWSGI协议，http协议

### 143.Django、Flask、Tornado的对比？
1、 Django走的大而全的方向，开发效率高。它的MTV框架，自带的ORM,admin后台管理,自带的sqlite数据库和开发测试用的服务器，给开发者提高了超高的开发效率。
重量级web框架，功能齐全，提供一站式解决的思路，能让开发者不用在选择上花费大量时间。

自带ORM和模板引擎，支持jinja等非官方模板引擎。

自带ORM使Django和关系型数据库耦合度高，如果要使用非关系型数据库，需要使用第三方库

自带数据库管理app

成熟，稳定，开发效率高，相对于Flask，Django的整体封闭性比较好，适合做企业级网站的开发。python web框架的先驱，第三方库丰富

2、 Flask 是轻量级的框架，自由，灵活，可扩展性强，核心基于Werkzeug WSGI工具 和jinja2 模板引擎

适用于做小网站以及web服务的API,开发大型网站无压力，但架构需要自己设计

与关系型数据库的结合不弱于Django，而与非关系型数据库的结合远远优于Django

3、 Tornado走的是少而精的方向，性能优越，它最出名的异步非阻塞的设计方式

Tornado的两大核心模块：

iostraem:对非阻塞的socket进行简单的封装

ioloop: 对I/O 多路复用的封装,它实现一个单例

### 144.CORS 和 CSRF的区别？
什么是CORS？

CORS是一个W3C标准,全称是“跨域资源共享"(Cross-origin resoure sharing).
它允许浏览器向跨源服务器，发出XMLHttpRequest请求，从而客服了AJAX只能同源使用的限制。

什么是CSRF？

CSRF主流防御方式是在后端生成表单的时候生成一串随机token,内置到表单里成为一个字段，同时，将此串token置入session中。每次表单提交到后端时都会检查这两个值是否一致，以此来判断此次表单提交是否是可信的，提交过一次之后，如果这个页面没有生成CSRF token,那么token将会被清空,如果有新的需求，那么token会被更新。
攻击者可以伪造POST表单提交，但是他没有后端生成的内置于表单的token，session中没有token都无济于事。

### 145.Session,Cookie,JWT的理解
为什么要使用会话管理

众所周知，HTTP协议是一个无状态的协议，也就是说每个请求都是一个独立的请求，请求与请求之间并无关系。但在实际的应用场景，这种方式并不能满足我们的需求。举个大家都喜欢用的例子，把商品加入购物车，单独考虑这个请求，服务端并不知道这个商品是谁的，应该加入谁的购物车？因此这个请求的上下文环境实际上应该包含用户的相关信息，在每次用户发出请求时把这一小部分额外信息，也做为请求的一部分，这样服务端就可以根据上下文中的信息，针对具体的用户进行操作。所以这几种技术的出现都是对HTTP协议的一个补充，使得我们可以用HTTP协议+状态管理构建一个的面向用户的WEB应用。

Session 和Cookie的区别

  这里我想先谈谈session与cookies,因为这两个技术是做为开发最为常见的。那么session与cookies的区别是什么？个人认为session与cookies最核心区别在于额外信息由谁来维护。利用cookies来实现会话管理时，用户的相关信息或者其他我们想要保持在每个请求中的信息，都是放在cookies中,而cookies是由客户端来保存，每当客户端发出新请求时，就会稍带上cookies,服务端会根据其中的信息进行操作。
  当利用session来进行会话管理时，客户端实际上只存了一个由服务端发送的session_id,而由这个session_id,可以在服务端还原出所需要的所有状态信息，从这里可以看出这部分信息是由服务端来维护的。

除此以外，session与cookies都有一些自己的缺点：
    
cookies的安全性不好，攻击者可以通过获取本地cookies进行欺骗或者利用cookies进行CSRF攻击。使用cookies时,在多个域名下，会存在跨域问题。
session 在一定的时间里，需要存放在服务端，因此当拥有大量用户时，也会大幅度降低服务端的性能，当有多台机器时，如何共享session也会是一个问题.(redis集群)也就是说，用户第一个访问的时候是服务器A，而第二个请求被转发给了服务器B，那服务器B如何得知其状态。实际上，session与cookies是有联系的，比如我们可以把session_id存放在cookies中的。

JWT是如何工作的

首先用户发出登录请求，服务端根据用户的登录请求进行匹配，如果匹配成功，将相关的信息放入payload中，利用算法，加上服务端的密钥生成token，这里需要注意的是secret_key很重要，如果这个泄露的话，客户端就可以随机篡改发送的额外信息，它是信息完整性的保证。生成token后服务端将其返回给客户端，客户端可以在下次请求时，将token一起交给服务端，一般是说我们可以将其放在Authorization首部中，这样也就可以避免跨域问题。

### 146.简述Django请求生命周期
一般是用户通过浏览器向我们的服务器发起一个请求(request),这个请求会去访问视图函数，如果不涉及到数据调用，那么这个时候视图函数返回一个模板也就是一个网页给用户）
视图函数调用模型毛模型去数据库查找数据，然后逐级返回，视图函数把返回的数据填充到模板中空格中，最后返回网页给用户。

1.wsgi ,请求封装后交给web框架（Flask，Django)

2.中间件，对请求进行校验或在请求对象中添加其他相关数据，例如：csrf,request.session

3.路由匹配 根据浏览器发送的不同url去匹配不同的视图函数

4.视图函数，在视图函数中进行业务逻辑的处理，可能涉及到：orm，templates 

5.中间件，对响应的数据进行处理

6.wsgi，将响应的内容发送给浏览器

### 147.用的restframework完成api发送时间时区
当前的问题是用django的rest framework模块做一个get请求的发送时间以及时区信息的api
```python
class getCurrenttime(APIView):
    def get(self,request):
        local_time = time.localtime()
        time_zone =settings.TIME_ZONE
        temp = {'localtime':local_time,'timezone':time_zone}
        return Response(temp)
```
### 148.nginx,tomcat,apach到都是什么？
Nginx（engine x)是一个高性能的HTTP和反向代理服务器，也是 一个IMAP/POP3/SMTP服务器，工作在OSI七层，负载的实现方式：轮询，IP_HASH,fair,session_sticky.
Apache HTTP Server是一个模块化的服务器，源于NCSAhttpd服务器
Tomcat 服务器是一个免费的开放源代码的Web应用服务器，属于轻量级应用服务器，是开发和调试JSP程序的首选。

### 149.请给出你熟悉关系数据库范式有哪些，有什么作用？
在进行数据库的设计时，所遵循的一些规范，只要按照设计规范进行设计，就能设计出没有数据冗余和数据维护异常的数据库结构。

数据库的设计的规范有很多，通常来说我们在设是数据库时只要达到其中一些规范就可以了，这些规范又称之为数据库的三范式，一共有三条，也存在着其他范式，我们只要做到满足前三个范式的要求，就能设陈出符合我们的数据库了，我们也不能全部来按照范式的要求来做，还要考虑实际的业务使用情况，所以有时候也需要做一些违反范式的要求。
1.数据库设计的第一范式(最基本)，基本上所有数据库的范式都是符合第一范式的，符合第一范式的表具有以下几个特点：

数据库表中的所有字段都只具有单一属性，单一属性的列是由基本的数据类型（整型，浮点型，字符型等）所构成的设计出来的表都是简单的二比表

2.数据库设计的第二范式(是在第一范式的基础上设计的)，要求一个表中只具有一个业务主键，也就是说符合第二范式的表中不能存在非主键列对只对部分主键的依赖关系

3.数据库设计的第三范式，指每一个非主属性既不部分依赖与也不传递依赖于业务主键，也就是第二范式的基础上消除了非主属性对主键的传递依赖

### 150.简述QQ登陆过程
qq登录，在我们的项目中分为了三个接口，

第一个接口是请求qq服务器返回一个qq登录的界面;

第二个接口是通过扫码或账号登陆进行验证，qq服务器返回给浏览器一个code和state,利用这个code通过本地服务器去向qq服务器获取access_token覆返回给本地服务器，凭借access_token再向qq服务器获取用户的openid(openid用户的唯一标识)

第三个接口是判断用户是否是第一次qq登录，如果不是的话直接登录返回的jwt-token给用户，对没有绑定过本网站的用户，对openid进行加密生成token进行绑定

### 151.post 和 get的区别?
1.GET是从服务器上获取数据，POST是向服务器传送数据

2.在客户端，GET方式在通过URL提交数据，数据在URL中可以看到，POST方式，数据放置在HTML——HEADER内提交

3.对于GET方式，服务器端用Request.QueryString获取变量的值，对于POST方式，服务器端用Request.Form获取提交的数据


### 152.项目中日志的作用
一、日志相关概念

1.日志是一种可以追踪某些软件运行时所发生事件的方法

2.软件开发人员可以向他们的代码中调用日志记录相关的方法来表明发生了某些事情

3.一个事件可以用一个包含可选变量数据的消息来描述

4.此外，事件也有重要性的概念，这个重要性也可以被成为严重性级别(level)

二、日志的作用

1.通过log的分析，可以方便用户了解系统或软件、应用的运行情况;

2.如果你的应用log足够丰富，可以分析以往用户的操作行为、类型喜好，地域分布或其他更多信息;

3.如果一个应用的log同时也分了多个级别，那么可以很轻易地分析得到该应用的健康状况，及时发现问题并快速定位、解决问题，补救损失。

4.简单来讲就是我们通过记录和分析日志可以了解一个系统或软件程序运行情况是否正常，也可以在应用程序出现故障时快速定位问题。不仅在开发中，在运维中日志也很重要，日志的作用也可以简单。总结为以下几点：

1.程序调试

2.了解软件程序运行情况，是否正常

3,软件程序运行故障分析与问题定位

4,如果应用的日志信息足够详细和丰富，还可以用来做用户行为分析

### 153.django中间件的使用？
Django在中间件中预置了六个方法，这六个方法的区别在于不同的阶段执行，对输入或输出进行干预，方法如下：

1.初始化：无需任何参数，服务器响应第一个请求的时候调用一次，用于确定是否启用当前中间件
```python
def __init__():
    pass
```
2.处理请求前：在每个请求上调用，返回None或HttpResponse对象。
```python
def process_request(request):
    pass
```
3.处理视图前:在每个请求上调用，返回None或HttpResponse对象。
```python
def process_view(request,view_func,view_args,view_kwargs):
    pass
```
4.处理模板响应前：在每个请求上调用，返回实现了render方法的响应对象。
```python
def process_template_response(request,response):
    pass
```
5.处理响应后：所有响应返回浏览器之前被调用，在每个请求上调用，返回HttpResponse对象。
```python
def process_response(request,response):
    pass
```
6.异常处理：当视图抛出异常时调用，在每个请求上调用，返回一个HttpResponse对象。
```python
def process_exception(request,exception):
    pass
```
### 154.谈一下你对uWSGI和nginx的理解？
1.uWSGI是一个Web服务器，它实现了WSGI协议、uwsgi、http等协议。Nginx中HttpUwsgiModule的作用是与uWSGI服务器进行交换。WSGI是一种Web服务器网关接口。它是一个Web服务器（如nginx，uWSGI等服务器）与web应用（如用Flask框架写的程序）通信的一种规范。

要注意WSGI/uwsgi/uWSGI这三个概念的区分。

WSGI是一种通信协议。

uwsgi是一种线路协议而不是通信协议，在此常用于在uWSGI服务器与其他网络服务器的数据通信。

uWSGI是实现了uwsgi和WSGI两种协议的Web服务器。

nginx 是一个开源的高性能的HTTP服务器和反向代理：

1.作为web服务器，它处理静态文件和索引文件效果非常高

2.它的设计非常注重效率，最大支持5万个并发连接，但只占用很少的内存空间

3.稳定性高，配置简洁。

4.强大的反向代理和负载均衡功能，平衡集群中各个服务器的负载压力应用

### 155.Python中三大框架各自的应用场景？
django:主要是用来搞快速开发的，他的亮点就是快速开发，节约成本，,如果要实现高并发的话，就要对django进行二次开发，比如把整个笨重的框架给拆掉自己写socket实现http的通信,底层用纯c,c++写提升效率，ORM框架给干掉，自己编写封装与数据库交互的框架,ORM虽然面向对象来操作数据库，但是它的效率很低，使用外键来联系表与表之间的查询;
flask: 轻量级，主要是用来写接口的一个框架，实现前后端分离，提考开发效率，Flask本身相当于一个内核，其他几乎所有的功能都要用到扩展(邮件扩展Flask-Mail，用户认证Flask-Login),都需要用第三方的扩展来实现。比如可以用Flask-extension加入ORM、文件上传、身份验证等。Flask没有默认使用的数据库，你可以选择MySQL，也可以用NoSQL。

其WSGI工具箱用Werkzeug(路由模块)，模板引擎则使用Jinja2,这两个也是Flask框架的核心。

Tornado： Tornado是一种Web服务器软件的开源版本。Tornado和现在的主流Web服务器框架（包括大多数Python的框架）有着明显的区别：它是非阻塞式服务器，而且速度相当快。得利于其非阻塞的方式和对epoll的运用，Tornado每秒可以处理数以千计的连接因此Tornado是实时Web服务的一个理想框架
### 156.Django中哪里用到了线程？哪里用到了协程？哪里用到了进程？
1.Django中耗时的任务用一个进程或者线程来执行，比如发邮件，使用celery.

2.部署django项目是时候，配置文件中设置了进程和协程的相关配置。

### 157.有用过Django REST framework吗？
Django REST framework是一个强大而灵活的Web API工具。使用RESTframework的理由有：

Web browsable API对开发者有极大的好处

包括OAuth1a和OAuth2的认证策略

支持ORM和非ORM数据资源的序列化

全程自定义开发--如果不想使用更加强大的功能，可仅仅使用常规的function-based views额外的文档和强大的社区支持
### 158.对cookies与session的了解？他们能单独用吗？
Session采用的是在服务器端保持状态的方案，而Cookie采用的是在客户端保持状态的方案。但是禁用Cookie就不能得到Session。因为Session是用Session ID来确定当前对话所对应的服务器Session，而Session ID是通过Cookie来传递的，禁用Cookie相当于SessionID,也就得不到Session。

## 爬虫
### 159.试列出至少三种目前流行的大型数据库
### 160.列举您使用过的Python网络爬虫所用到的网络数据包?

requests, urllib,urllib2, httplib2

### 161.爬取数据后使用哪个数据库存储数据的，为什么？

### 162.你用过的爬虫框架或者模块有哪些？优缺点？

Python自带：urllib,urllib2

第三方：requests

框架： Scrapy

urllib 和urllib2模块都做与请求URL相关的操作，但他们提供不同的功能。

urllib2: urllib2.urlopen可以接受一个Request对象或者url,(在接受Request对象时，并以此可以来设置一个URL的headers),urllib.urlopen只接收一个url。

urllib 有urlencode,urllib2没有，因此总是urllib, urllib2常会一起使用的原因

scrapy是封装起来的框架，他包含了下载器，解析器，日志及异常处理，基于多线程，twisted的方式处理，对于固定单个网站的爬取开发，有优势，但是对于多网站爬取100个网站，并发及分布式处理不够灵活，不便调整与扩展

requests是一个HTTP库，它只是用来请求，它是一个强大的库，下载，解析全部自己处理，灵活性高

Scrapy优点：异步，xpath，强大的统计和log系统，支持不同url。shell方便独立调试。写middleware方便过滤。通过管道存入数据库

### 163.写爬虫是用多进程好？还是多线程好？
### 164.常见的反爬虫和应对方法？
### 165.解析网页的解析器使用最多的是哪几个?
### 166.需要登录的网页，如何解决同时限制ip，cookie,session
### 167.验证码的解决?
### 168.使用最多的数据库，对他们的理解？
### 169.编写过哪些爬虫中间件？
### 170.“极验”滑动验证码如何破解？
### 171.爬虫多久爬一次，爬下来的数据是怎么存储？
### 172.cookie过期的处理问题？
### 173.动态加载又对及时性要求很高怎么处理？
### 174.HTTPS有什么优点和缺点？
### 175.HTTPS是如何实现安全传输数据的？
### 176.TTL，MSL，RTT各是什么？
### 177.谈一谈你对Selenium和PhantomJS了解
### 178.平常怎么使用代理的 ？
### 179.存放在数据库(redis、mysql等)。
### 180.怎么监控爬虫的状态?
### 181.描述下scrapy框架运行的机制？
### 182.谈谈你对Scrapy的理解？
### 183.怎么样让 scrapy 框架发送一个 post 请求（具体写出来）
### 184.怎么监控爬虫的状态 ？
### 185.怎么判断网站是否更新？
### 186.图片、视频爬取怎么绕过防盗连接
### 187.你爬出来的数据量大概有多大？大概多长时间爬一次？
### 188.用什么数据库存爬下来的数据？部署是你做的吗？怎么部署？
### 189.增量爬取
### 190.爬取下来的数据如何去重，说一下scrapy的具体的算法依据。
### 191.Scrapy的优缺点?
### 192.怎么设置爬取深度？
### 193.scrapy和scrapy-redis有什么区别？为什么选择redis数据库？
### 194.分布式爬虫主要解决什么问题？
### 195.什么是分布式存储？
### 196.你所知道的分布式爬虫方案有哪些？
### 197.scrapy-redis，有做过其他的分布式爬虫吗？

# 数据库
## MySQL
### 198.主键 超键 候选键 外键

主键：数据库表中对存储数据对象予以唯一和完整标识的数据列或属性的组合。一个数据列只能有一个主键，且主键的取值不能缺失，即不能为空值(Null).

超键：在关系中能唯一标识元组的属性集称为关系模式的超键。一个属性可以作为一个超键，多个属性组合在一起也可以作为一个超键。超键包含候选键和主键。

候选键：是最小超键，即没有冗余元素的超键��

外键：在一个表中存在的另一个表的主键称此表的外键。

### 199.视图的作用，视图可以更改么？

视图是虚拟的表，与包含数据的表不一样，视图只包含使用时动态检索数据的查询;不包含任何列或数据。使用视图可以简化复杂的sql操作，隐藏具体的细节，保护数据;视图创建后，可以使用与表相同的方式利用它们。

视图不能被索引，也不能有关联的触发器或默认值，如果视图本身内有order by则对视图再次order by将被覆盖。

创建视图： create view xxx as xxxxxx

对于某些视图比如未使用联结子查询分组聚集函数Distinct Union等，是可以对其更新的，对视图的更新将对基表进行更新;但是视图主要用于简化检索，保护数据，并不用于更新，而且大部分视图都不可以更新。

### 200.drop,delete与truncate的区别

drop直接删掉表，truncate删除表中数据，再插入时自增长id又从1开始，delete删除表中数据，可以加where字句。

1.delete 语句执行删除的过程是每次从表中删除一行，并且同时将该行的删除操作作为事务记录在日志中保存以便进行回滚操作。truncate table则一次性地从表中删除所有的数据并不把单独的删除操作记录记入日志保存，删除行是不能恢复的。并且在删除的过程中不会激活与表有关的删除触发器，执行速度快。

2.表和索引所占空间。当表被truncate后，这个表和索引所占用的空间会恢复到初始大小，而delete操作不会减少表或索引所占用的空间。drop语句将表所占用的空间全释放掉。

3.一般而言，drop>truncate>delete

4.应用范围。truncate只能对table，delete可以是table和view

5.truncate和delete只删除数据，而drop则删除整个表（结构和数据)

6.truncate与不带where的delete:只删除数据，而不删除表的结构（定义）drop语句将删除表的结构被依赖的约束(constrain),触发器（trigger)索引(index);依赖于该表的存储过程/函数将被保留，但其状态会变为:invalid.

### 201.索引的工作原理及其种类

数据库索引，是数据库管理系统中一个排序的数据结构，以协助快速查询，更新数据库表中数据。索引的实现通常使用B树以其变种B+树。

在数据之外，数据库系统还维护着满足特定查找算法的数据结构，这些数据结构以某种方式引用（指向）数据，这样就可以在这些数据结构上实现高级查找算法。这种数据结构，就是索引。

为表设置索引要付出代价的：一是增加了数据库的存储空间，二是在插入和修改数据时要花费较多的时间（因为索引也要随之变动）

### 202.连接的种类
### 203.数据库优化的思路
### 204.存储过程与触发器的区别
### 205.悲观锁和乐观锁是什么？
### 206.你常用的mysql引擎有哪些?各引擎间有什么区别?

## Redis
### 207.Redis宕机怎么解决?

宕机:服务器停止服务‘

如果只有一台redis，肯定 会造成数据丢失，无法挽救

多台redis或者是redis集群，宕机则需要分为在主从模式下区分来看：

slave从redis宕机，配置主从复制的时候才配置从的redis，从的会从主的redis中读取主的redis的操作日志1，在redis中从库重新启动后会自动加入到主从架构中，自动完成同步数据;

2, 如果从数据库实现了持久化，此时千万不要立马重启服务，否则可能会造成数据丢失，正确的操作如下：在slave数据上执行SLAVEOF ON ONE,来断开主从关系并把slave升级为主库，此时重新启动主数据库，执行SLAVEOF，把它设置为从库，连接到主的redis上面做主从复制，自动备份数据。

以上过程很容易配置错误，可以使用redis提供的哨兵机制来简化上面的操作。简单的方法:redis的哨兵(sentinel)的功能

### 208.redis和mecached的区别，以及使用场景

区别

1、redis和Memcache都是将数据存放在内存中，都是内存数据库。不过memcache还可以用于缓存其他东西，例如图片，视频等等

2、Redis不仅仅支持简单的k/v类型的数据，同时还提供list,set,hash等数据结构的存储

3、虚拟内存-redis当物流内存用完时，可以将一些很久没用的value交换到磁盘

4、过期策略-memcache在set时就指定，例如set key1 0 0 8，即永不过期。Redis可以通过例如expire设定，例如expire name 10

5、分布式-设定memcache集群，利用magent做一主多从，redis可以做一主多从。都可以一主一丛

6、存储数据安全-memcache挂掉后，数据没了，redis可以定期保存到磁盘(持久化)

7、灾难恢复-memcache挂掉后，数据不可恢复，redis数据丢失后可以通过aof恢复

8、Redis支持数据的备份，即master-slave模式的数据备份

9、应用场景不一样，redis除了作为NoSQL数据库使用外，还能用做消息队列，数据堆栈和数据缓存等;Memcache适合于缓存SQL语句，数据集，用户临时性数据，延迟查询数据和session等

使用场景

1,如果有持久方面的需求或对数据类型和处理有要求的应该选择redis

2,如果简单的key/value存储应该选择memcached.

### 209.Redis集群方案该怎么做?都有哪些方案?

1,codis

目前用的最多的集群方案，基本和twemproxy一致的效果，但它支持在节点数量改变情况下，旧节点数据客恢复到新hash节点

2redis cluster3.0自带的集群，特点在于他的分布式算法不是一致性hash，而是hash槽的概念，以及自身支持节点设置从节点。具体看官方介绍

3.在业务代码层实现，起几个毫无关联的redis实例，在代码层，对key进行hash计算，然后去对应的redis实例操作数据。这种方式对hash层代码要求比较高，考虑部分包括，节点失效后的替代算法方案，数据震荡后的字典脚本恢复，实例的监控，等等

### 210.Redis回收进程是如何工作的

一个客户端运行了新的命令，添加了新的数据。

redis检查内存使用情况，如果大于maxmemory的限制，则根据设定好的策略进行回收。

一个新的命令被执行等等，所以我们不断地穿越内存限制的边界，通过不断达到边界然后不断回收回到边界以下。

如果一个命令的结果导致大量内存被使用(例如很大的集合的交集保存到一个新的键)，不用多久内存限制就会被这个内存使用量超越。

## MongoDB
### 211.MongoDB中对多条记录做更新操作命令是什么？
### 212.MongoDB如何才会拓展到多个shard里？

## 测试
### 213.编写测试计划的目的是
### 214.对关键词触发模块进行测试
### 215.其他常用笔试题目网址汇总
### 216.测试人员在软件开发过程中的任务是什么
### 217.一条软件Bug记录都包含了哪些内容？
### 218.简述黑盒测试和白盒测试的优缺点
### 219.请列出你所知道的软件测试种类，至少5项
### 220.Alpha测试与Beta测试的区别是什么？
### 221.举例说明什么是Bug？一个bug report应包含什么关键字？

## 数据结构
### 222.数组中出现次数超过一半的数字-Python版
### 223.求100以内的质数
### 224.无重复字符的最长子串-Python实现
### 225.通过2个5/6升得水壶从池塘得到3升水
### 226.什么是MD5加密，有什么特点？
### 227.什么是对称加密和非对称加密
### 228.冒泡排序的思想？
### 229.快速排序的思想？
### 230.如何判断单向链表中是否有环？
### 231.你知道哪些排序算法（一般是通过问题考算法）
### 232.斐波那契数列

**数列定义: **

f 0 = f 1 = 1
f n = f (n-1) + f (n-2)

#### 根据定义

速度很慢，另外(暴栈注意！⚠️️） `O(fibonacci n)`

```python
def fibonacci(n):
    if n == 0 or n == 1:
        return 1
    return fibonacci(n - 1) + fibonacci(n - 2)
```

#### 线性时间的

**状态/循环**

```python
def fibonacci(n):
   a, b = 1, 1
   for _ in range(n):
       a, b = b, a + b
   return a
```

**递归**

```python
def fibonacci(n):
    def fib(n_, s):
        if n_ == 0:
            return s[0]
        a, b = s
        return fib(n_ - 1, (b, a + b))
    return fib(n, (1, 1))
```

**map(zipwith)**

```python
def fibs():
    yield 1
    fibs_ = fibs()
    yield next(fibs_)
    fibs__ = fibs()
    for fib in map(lambad a, b: a + b, fibs_, fibs__):
        yield fib
        
        
def fibonacci(n):
    fibs_ = fibs()
    for _ in range(n):
        next(fibs_)
    return next(fibs)
```

**做缓存**

```python
def cache(fn):
    cached = {}
    def wrapper(*args):
        if args not in cached:
            cached[args] = fn(*args)
        return cached[args]
    wrapper.__name__ = fn.__name__
    return wrapper

@cache
def fib(n):
    if n < 2:
        return 1
    return fib(n-1) + fib(n-2)
```

**利用 funtools.lru_cache 做缓存**

```python
from functools import lru_cache

@lru_cache(maxsize=32)
def fib(n):
    if n < 2:
        return 1
    return fib(n-1) + fib(n-2)
```

#### Logarithmic

**矩阵**

```python
import numpy as np
def fibonacci(n):
    return (np.matrix([[0, 1], [1, 1]]) ** n)[1, 1]
```

**不是矩阵**

```python
def fibonacci(n):
    def fib(n):
        if n == 0:
            return (1, 1)
        elif n == 1:
            return (1, 2)
        a, b = fib(n // 2 - 1)
        c = a + b
        if n % 2 == 0:
            return (a * a + b * b, c * c - a * a)
        return (c * c - a * a, b * b + c * c)
    return fib(n)[0]
```

### 233.如何翻转一个单链表？

```python
class Node:
    def __init__(self,data=None,next=None):
        self.data = data
        self.next = next
        
def rev(link):
    pre = link
    cur = link.next
    pre.next = None
    while cur:
        temp  = cur.next
        cur.next = pre
        pre = cur
        cur = tmp
    return pre

if __name__ == '__main__':
    link = Node(1,Node(2,Node(3,Node(4,Node(5,Node(6,Node7,Node(8.Node(9))))))))
    root = rev(link)
    while root:
        print(roo.data)
        root = root.next
```



### 234.青蛙跳台阶问题

一只青蛙要跳上n层高的台阶，一次能跳一级，也可以跳两级，请问这只青蛙有多少种跳上这个n层台阶的方法？

方法1：递归

设青蛙跳上n级台阶有f(n)种方法，把这n种方法分为两大类，第一种最后一次跳了一级台阶，这类共有f(n-1)种，第二种最后一次跳了两级台阶，这种方法共有f(n-2)种，则得出递推公式f(n)=f(n-1) + f(n-2),显然f(1)=1,f(2)=2，这种方法虽然代码简单，但效率低，会超出时间上限

```python
class Solution:
    def climbStairs(self,n):
        if n ==1:
            return 1
        elif n==2:
            return 2
        else:
            return self.climbStairs(n-1) + self.climbStairs(n-2)
```

方法2：用循环来代替递归

```python
class Solution:
    def climbStairs(self,n):
        if n==1 or n==2:
            return n
        a,b,c = 1,2,3
        for i in range(3,n+1):
            c = a+b
            a = b
            b = c
        return c
```

### 235.两数之和 Two Sum



### 236.搜索旋转排序数组 Search in Rotated Sorted Array
### 237.Python实现一个Stack的数据结构
### 238.写一个二分查找
### 239.set 用 in 时间复杂度是多少，为什么？
### 240.列表中有n个正整数范围在[0，1000]，进行排序；
### 241.面向对象编程中有组合和继承的方法实现新的类
## 大数据
### 242.找出1G的文件中高频词
### 243.一个大约有一万行的文本文件统计高频词
### 244.怎么在海量数据中找出重复次数最多的一个？
### 245.判断数据是否在大量数据中

## 架构

### [Python后端架构演进](<https://zhu327.github.io/2018/07/19/python%E5%90%8E%E7%AB%AF%E6%9E%B6%E6%9E%84%E6%BC%94%E8%BF%9B/>)

这篇文章几乎涵盖了python会用的架构，在面试可以手画架构图，根据自己的项目谈下技术选型和优劣，遇到的坑等。绝对加分
