# 变量

```dart
// dart可自动推断变量类型
var name = '张三';

// 也可以主动给予类型,注意，带有给定类型时，var 符号取消
String name = '张三';

// 如果变量可能为空，我们要加上 ? 符号
String? name = null;

//不可变变量
final String name = '张三';

// 常量
const String name = '张三';
```

一个不可变的，可能为空的，字符串类型的变量：

```dart
final String? name = '张三';
```
## 数据类型
### 数字类型
- int：默认是 int64

```dart
int age = 18;
```

- double：默认是 float64

```dart
double height = 1.75;
```
### 字符串
- String

```dart
String name = '张三';
```
### 布尔类型
- bool

```dart
bool isMale = true;
```
### 数组
- List

```dart
List<String> names = ['张三', '李四', '王五'];
List<int> ages = [18, 19, 20];
```
### 字典
- Map

```dart
Map<String, String> user = {'name': '张三', 'age': '18'};
Map<String, int> user = {'name': '张三', 'age': 18};
Map<String, dynamic> user = {'name': '张三', 'age': 18};

```
## 运算符
### 算术运算符
```dart
int a = 1;
int b = 2;

int c = a + b; // +
int d = a - b; // - 
int e = a * b; // *
int f = a / b; // /
int g = a % b; // 取余
int h = a ~/ b; // 取整
```
### 关系运算符
```dart
int a = 1;
int b = 2;

bool c = a > b;
bool d = a < b;
bool e = a >= b;
bool f = a <= b;
bool g = a == b;
bool h = a != b;
```
### 逻辑运算符
```dart
bool a = true;
bool b = false;

bool c = a && b; // false
bool d = a || b; // true
bool e = !a; // false
```
### 赋值运算符
```dart
int a = 1;
int b = 2;

a += b;
a -= b;
a *= b;
a /= b;
a %= b;
a ~/= b;
```
### 条件运算符
- 三元运算符 ?:
- ?? 用于在第一个操作数为 null 时返回第二个操作数
- ??=  空值判断赋值，只在左值为 null 的情况下才执行赋值操作


```dart
int a = 1;
int b = 2;

int c = a > b ? a : b; // a 如果大于 b，则返回 a，否则返回 b
```
```dart
int a = 1;
int b = null;

int c = b ?? a; // ?? 用于在第一个操作数为null时返回第二个操作数
```
```dart
int a = 1;
int b = null;
b ??= a;
```

### 类型测试运算符

判断变量的类型
- is a 变量是 xx 类型
- is！a 变量不是 xx 类型
- as a 变量强制转换为 xx 类型
```dart
int a = 1;

if (a is int) {
  print('a 是 int 类型');
}

if (a is! int) {
  print('a 不是 int 类型');
}

a = a as int;
print(a);
```

### 位运算
```dart
int a = 8; 1000
int b = 2; 10

int c = a & b; // 与运算 都是1才为1 ：0 
int d = a | b; // 或运算 有一个为1则为1 ：1010 （10）
int e = a ^ b; // 异或运算 两个位相同则为0 两个位不同则为1 ：1010 （10）
int f = ~a; // 非运算 取反 ：-7
int g = a << b; // 左移运算 100000 ：（32）
int h = a >> b; // 右移运算 10： 2
```
### 函数操作符
- ..  级联操作符，用于对同一对象执行一系列操作 (链式操作)，避免创建多余的临时变量
- ?. 点符号前加问号，表示当前调用只在被访问者不为 null 的情况下才执行

```dart
// 不使用级联
person.name = 'bob'; person.age = 28; 
//使用级联：
person..name = 'bob' ..age = 28;
```
```dart
var upper = name?.toUpperCase();
```