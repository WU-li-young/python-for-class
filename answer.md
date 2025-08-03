## 答案
這裡是練習的參考答案，每個城市都有很多種寫法，不一定要和我寫的一樣，若是能正確輸出就都可以。這裡提供的答案僅供參考，若要正確且快速的學習程式，建議不要先看解答，先自己寫，寫久了有手感自然就會了。加油!

## 第一支程式
### 基礎題
題目:
請印出"I Love Python."
參考解答:
```
print("I Love Python.")
```

## 變數
### 基礎題
題目:
1. 宣告五個變數，分別是整數,浮點數,字串,字元，其值為1,1.0,1,a，並輸出它們。
2. 使用 type() 印出每個變數的型態。
參考答案:
```
a = 1
b = 1.0
c = "1"
print(a)
print(b)
print(c)
print(type(a))
print(type(b))
print(type(c))
```

### 進階題
題目:
將字串`"123"`轉成整數，並乘以 2 後印出結果與型態。
參考解答:
```
a = "123"
print(int(a)*2)
```

## 輸出輸入
### 基礎題
題目:
請讓使用者輸入一個名字(xxx)，然後輸出「Hello, xxx!」。
參考解答:
```
name = input()
print("Hello, %s!"%name)
```

### 進階題
題目:
輸出一段格式化文字，顯示：「姓名: 小明，成績: 87」，使用 %s 和 %d。
參考解答:
```
name = "小明"
score = 87 
print("姓名: %s，成績: %d"%(name,score))
```

### 挑戰題
題目:
讓使用者輸入名字和成績，並用格式化方式印出：「[名字] 的成績是 [成績] 分」。
參考解答:
```
name = input()
score = eval(input())
print("%s的成績是%d分"%(name,score))
```
## 運算子
### 基礎題
題目:
1. 請計算以下數學式並印出結果：9 除以 2、9 除以 2 取整數、9 餘 2。
2. 請比較 5 >= 3 是否為真，並印出結果。
參考答案:
```
print(9/2,9//2,9%2)
print(5>=3)
```
## 條件式
### 基礎題
題目:
1. 輸入一個分數，若大於等於 60，印出「及格」。
2. 使用 if-elif-else 判斷一個分數的等第（A/B/C/F）。
參考解答:
```
score = eval(input())
if score >= 60:
    print("及格")
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else:
    print("F")
```
## 陣列與字串
題目:
1. 建立一個陣列 [10, 20, 30] 並印出第一個元素。
2. 建立字串 "Python"，印出其中的第 3 個字母。
參考解答:
```
lst = [10, 20, 30]
string = "Python"
print(lst[0])
print(string[2])
```
### 進階題
題目:
使用 len() 和 sum() 分別取得 [1, 2, 3, 4] 的長度與總和。
```
lst = [1, 2, 3, 4]
print("長度:", len(lst))
print("總和:", sum(lst))
```

### 挑戰題
題目:
使用 .append() 加入一筆資料到陣列，再使用 .pop() 刪除最後一筆資料並印出最終陣列。
```
lst = [1, 2, 3]
print("加入前:", lst)
lst.append(4)
print("加入後:", lst)
lst.pop()
print("刪除後:", lst)
```

## 迴圈
### 基礎題
題目:
1. 用 for 印出從 1 到 5 的數字。
2. 用 while 印出從 1 到 5 的數字。
參考答案:
```
for i in range(1, 6):
    print(i)
j = 1
while j <= 5:
    print(j)
    i += 1
```

### 進階題
題目:
1. 使用 for 加 range(0, 10, 2) 印出偶數。
2. 印出一個列表中的所有項目 [10,20,30]。
參考答案:
```
lst = [10, 20, 30]
for i in range(0, 10, 2):
    print(i)
for j in lst:
    print(j)
```

### 挑戰題
題目:
用迴圈計算從 1 加到 100 的總和。
參考答案:
```
sum = 0
for i in range (1,101):
    sum += i
print(sum)
```

## 函式
### 基礎題
題目:
1. 自訂一個函式 hello()，印出 "Hello!"。
2. 定義一個函式 square(n)，回傳 n 的平方。
參考解答:
```
def hello():
    print("Hello!")
def square(n):
    return n **2
hello()
print(square(5))
```

### 進階題
題目:
定義一個函式 calculator(a, b, op)，op 可為 + - * /，根據 op 計算 a 與 b 的結果。
參考答案:
```
def calculator(a, b, op):
    if op == "+":
        return a + b
    elif op == "-":
        return a - b
    elif op == "*":
        return a * b
    elif op == "/":
        if b == 0:
            return "錯誤：除以 0"
        return a / b
    else:
        return "不支援的運算符號"

x = int(input())
y = int(input())
operator = input()
print(calculator(x, y, operator))
```

## 複習題(統整)
### 第一題 簡易學生成績分析系統
參考答案:
```
names = []
scores = []

n = int(input("請輸入學生人數："))

for i in range(n):
    name = input(f"請輸入第{i+1}位學生姓名：")
    score = int(input(f"請輸入{name}的成績："))
    names.append(name)
    scores.append(score)

print("學生成績：")
for i in range(n):
    print(f"{names[i]}：{scores[i]}分")

average = sum(scores) / n
print(f"平均成績：{average:.1f}分")

max_score = max(scores)
min_score = min(scores)
max_index = scores.index(max_score)
min_index = scores.index(min_score)

print(f"最高分：{names[max_index]}（{max_score}分）")
print(f"最低分：{names[min_index]}（{min_score}分）")
```