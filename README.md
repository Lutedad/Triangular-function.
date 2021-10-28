import time
import math
while True:
    choose = input('사용하실 삼각함수의 덧셈정리를 골라주세요 (sin/cos/tan) \n또는 삼각함수의 값을 구하실려면 (tf)) \n 삼각비 표를 보고 싶으시다면 (tft):\n 끝내실려면 (quit)')
    def sin(a):
            a = math.radians(a)                               #import를 배우지 않은 상태에서 만듦.
            result=math.sin(a)
            return result
    def sin(b):
            b = math.radians(b)
            result=math.sin(b)
            return result
    def cos(a):
            a = math.radians(a)
            result=math.cos(a)
            return result
    def cos(b):
            a = math.radians(b)
            result=math.cos(b)
            return result
    def tan(a):
            a = math.radians(a)
            result = math.tan(a)
            return result
    def tan(b):
            b = math.radians(b)
            result = math.tan(b)
            return result
    if choose == 'sin':
        a = int(input('1번째 Sin의 각을 입력하세요.:')) #=== Sin A에서 A
        b = int(input('2번째 Sin의 각을 입력하세요.:')) #=== Sin B에서 B
        plusminus = input('사용하실 부호를 선택하세요 (+,-):')
        if plusminus == '+':
            hap = sin(a)*cos(b)+cos(a)*sin(b)
            hap = round(hap,2)
            print(hap)
        if plusminus == '-':
            cha = sin(a)*cos(b)-cos(a)*sin(b)
            cha = round(cha,2)
            print(cha)
    if choose == 'cos':    
        a = int(input('1번째 Cos의 각을 입력하세요.:')) #=== Cos A에서 A
        b = int(input('2번째 Cos의 각을 입력하세요.:')) #=== Cos B에서 B
        plusminus = input('사용하실 부호를 선택하세요 (+,-):')
        if plusminus == '+':
            hap = cos(a)*cos(b)-sin(a)*sin(b)
            hap = round(hap,2)
            print(hap)
        if plusminus == '-':
            cha = cos(a)*cos(b)+sin(a)*sin(b)
            cha = round(cha,2)
            print(cha)
    if choose == 'tan':    
        a = int(input('1번째 Tan의 각을 입력하세요.:')) #=== Tan A에서 A
        b = int(input('2번째 Tan의 각을 입력하세요.:')) #=== Tan B에서 B
        plusminus = input('사용하실 부호를 선택하세요 (+,-):')
        if plusminus == '+':
            hap = (tan(a)+tan(b))/(1-tan(a)*tan(b))
            hap = round(hap,2)
            print(hap)
        if plusminus == '-':
            cha = (tan(a)-tan(b))/(1+tan(a)*tan(b))
            cha = round(cha,2)
            print(cha)
    if choose == 'quit':
        print('잘가요, 수고했어요')
        time.sleep(1.5)
        break
    if choose == 'tf':
        t= input('구하고 싶으신 삼각함수의 종류를 적어주세요 (sin,cos,tan):')
        t2 = int(input('각도를 적어주세요.:'))
        if t=='sin':
            t2 = math.radians(t2)
            t3 = math.sin(t2)
            print(round(t3, 2))
        if t=='cos':
            t2 = math.radians(t2)
            t3 = math.cos(t2)
            print(round(t3, 2))
        if t=='tan':
            t2 = math.radians(t2)
            t3 = math.tan(t2)
            print(round(t3, 2))
    if choose == 'tft':                                            #이 부분은 인터넷에서 퍼온 소스임, 추후 복습이 필요함. 2021/10/27(복습완료)
        print(" X     sinX      cosX      tanX")
        print("===================================")
        for i in range(0,91):
            sinx = round(math.sin(math.pi * (i/180)),4)   #math.pi * (i/180) 이거는 i = math.radians(i);t3 = math.tan(i)랑 똑같음
            cosx = round(math.cos(math.pi * (i/180)),4)
            tanx = round(math.tan(math.pi * (i/180)),4)
            print("{} ㅣ  {}  ㅣ  {}  ㅣ  {}".format(i, sinx, cosx, tanx))
            print("===================================")
print('잘가요, 수고했어요')
