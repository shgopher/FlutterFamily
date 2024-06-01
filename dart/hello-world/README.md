<!--
 * @Author: shgopher shgopher@gmail.com
 * @Date: 2024-06-01 12:27:14
 * @LastEditors: shgopher shgopher@gmail.com
 * @LastEditTime: 2024-06-01 12:31:31
 * @FilePath: /FlutterFamily/dart/hello-world/README.md
 * @Description: 
 * 
 * Copyright (c) 2024 by shgopher, All Rights Reserved. 
-->
# hello world

```dart
// Dart 程序的入口点
void main() async {
  // 变量声明
  var message = 'Hello, Dart!';
  print(message);

  // 基本数据类型
  int number = 42;
  double pi = 3.14159;
  bool isTrue = true;

  // 控制流：if 语句
  if (isTrue) {
    print('This is true!');
  }

  // 控制流：for 循环
  for (int i = 0; i < 5; i++) {
    print('Loop $i');
  }

  // 控制流：while 循环
  int count = 0;
  while (count < 3) {
    print('Count is $count');
    count++;
  }

  // 函数定义
  void greet(String name) {
    print('Hello, $name!');
  }
  
  // 调用函数
  greet('Dart');

  // 类定义
  class Person {
    String name;
    int age;

    Person(this.name, this.age);

    // 方法
    void introduce() {
      print('My name is $name and I am $age years old.');
    }
  }

  // 创建对象
  Person person = Person('Alice', 30);

  // 调用对象的方法
  person.introduce();

  // 异步编程：Future
  Future<void> fetchUserData() async {
    var user = await getUser();
    print('User: ${user.name}');
  }

  // 模拟异步获取用户数据
  Future<User> getUser() async {
    await Future.delayed(Duration(seconds: 1)); // 模拟网络延迟
    return User('Bob', 25);
  }

  // 错误处理
  try {
    await fetchUserData();
  } catch (e) {
    print('An error occurred: $e');
  }
}

// 模拟 User 类
class User {
  String name;
  int age;

  User(this.name, this.age);
}
```
