# 문자열 조작 알고리즘

문자열 조작 알고리즘은 문자열을 처리하고 변형하는 다양한 방법을 제공합니다. 이 문서에서는 몇 가지 기본적인 문자열 조작 기법과 그 예제를 설명합니다.

## 1. 문자열 반전

문자열을 반전시키는 방법은 다음과 같습니다.

```python
def reverse_string(s):
    return s[::-1]

# 예제
original = "Hello, World!"
reversed_string = reverse_string(original)
print(reversed_string)  # !dlroW ,olleH
```

## 2. 문자열 연결

여러 문자열을 연결하는 방법은 다음과 같습니다.

```python
def concatenate_strings(str1, str2):
    return str1 + str2

# 예제
string1 = "Hello"
string2 = "World"
result = concatenate_strings(string1, string2)
print(result)  # HelloWorld
```

## 3. 문자열 검색

문자열 내에서 특정 문자를 검색하는 방법은 다음과 같습니다.

```python
def find_character(s, char):
    return s.find(char)

# 예제
text = "Hello, World!"
index = find_character(text, 'W')
print(index)  # 7
```

## 4. 대소문자 변환

문자열의 대소문자를 변환하는 방법은 다음과 같습니다.

```python
def toggle_case(s):
    return s.swapcase()

# 예제
original = "Hello, World!"
toggled = toggle_case(original)
print(toggled)  # hELLO, wORLD!
```

## 5. 문자열 분할

문자열을 특정 구분자를 기준으로 분할하는 방법은 다음과 같습니다.

```python
def split_string(s, delimiter):
    return s.split(delimiter)

# 예제
text = "apple,banana,cherry"
fruits = split_string(text, ',')
print(fruits)  # ['apple', 'banana', 'cherry']
```

이 외에도 다양한 문자열 조작 기법이 있으며, 필요에 따라 적절한 방법을 선택하여 사용할 수 있습니다.