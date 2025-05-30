# 파이썬의 입력과 출력 - 프로그램의 입력과 출력

## 📚 sys.argv로 커맨드 라인 인자 처리하기

sys.argv는 Python에서 프로그램을 실행할 때 명령어 라인에서 인자를 받아오는 방법입니다.  
주로 스크립트를 실행할 때 사용자가 프로그램에 값을 넘겨주고, 그 값을 프로그램 내에서 처리하는 방식입니다.

---

## 📚 예시

```python
# example.py
import sys

args = sys.argv[1:]  # 첫 번째 인자는 스크립트 이름이기 때문에 [1:]로 슬라이싱하여 인자만 받음
for i in args:
    print(i.upper(), end=' ')
```

---

## 📚 설명

1) `import sys`  
   sys 모듈을 가져옵니다.  
   sys.argv는 프로그램을 실행할 때 전달된 인자들을 받을 수 있도록 도와주는 기능을 합니다.

2) `args = sys.argv[1:]`  
   sys.argv는 명령어로 입력된 모든 값을 리스트 형태로 저장합니다.  
   이때 `sys.argv[0]`은 항상 스크립트 이름이기 때문에, 우리가 실제로 입력한 인자만 받기 위해 `sys.argv[1:]`로 슬라이싱하여 가져옵니다.

3) `for i in args:`  
   args 리스트에 저장된 값들을 하나씩 반복문을 통해 처리합니다.

4) `print(i.upper(), end=' ')`  
   각 인자를 `upper()` 메서드를 이용해 대문자로 변환하고, 출력할 때 `end=' '`를 사용하여 공백을 삽입합니다.  
   기본적으로 `print()` 함수는 출력 후 줄 바꿈을 하지만, `end=' '`를 사용하면 한 줄에 여러 값을 출력할 수 있습니다.

---

## 📚 실행 방법

이 코드를 `example.py`라는 파일에 저장한 후, 커맨드 라인(명령 프롬프트)에서 실행합니다.

```
C:\user> python example.py hello world
```

**결과**

```
HELLO WORLD
```

위 코드에서 `hello`와 `world`는 명령어 뒤에 입력된 인자들이고, 프로그램은 이 인자들을 받아 대문자로 변환하여 출력합니다.
