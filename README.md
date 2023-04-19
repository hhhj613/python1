#파이썬 for문 짝수값 홀수값 구별하기

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]

even_numbers = []
odd_numbers = []

for number in numbers:
    if number % 2 == 0:
        even_numbers.append(number)
    else:
        odd_numbers.append(number)

print("Even numbers:", even_numbers)
print("Odd numbers:", odd_numbers)




#튜플 자료형으로 평균 점수 내기

# 점수 튜플
scores = (80, 90, 85, 95, 70)

# 평균 계산
average = sum(scores) / len(scores)

# 결과 출력
print("평균 점수는", average, "입니다.")



#for문과 range문을 이용한 구구단

for i in range(2,10):        # 1번 for문
...     for j in range(1, 10):   # 2번 for문
...         print(i*j, end=" ") 
...     print('') 


#점수 등수 매기기

scores = {"Alice": 80, "Bob": 70, "Charlie": 90, "David": 85}

sorted_scores = sorted(scores.items(), key=lambda x: x[1], reverse=True)

rank = 1
for i, (name, score) in enumerate(sorted_scores):
    if i > 0 and score < sorted_scores[i-1][1]:
        rank = i + 1
    print(f"{name}의 점수는 {score}점이고, 등수는 {rank}등입니다.")
    
    
    #커피자판기이야기
    coffee = 10
>>> money = 300
>>> while money:
...     print("돈을 받았으니 커피를 줍니다.")
...     coffee = coffee -1
...     print("남은 커피의 양은 %d개입니다." % coffee)
...     if coffee == 0:
...         print("커피가 다 떨어졌습니다. 판매를 중지합니다.")
...         break
...

#커피자판기이야기2
ccoffee = 10
while True:
    money = int(input("돈을 넣어 주세요: "))
    if money == 300:
        print("커피를 줍니다.")
        coffee = coffee -1
    elif money > 300:
        print("거스름돈 %d를 주고 커피를 줍니다." % (money -300))
        coffee = coffee -1
    else:
        print("돈을 다시 돌려주고 커피를 주지 않습니다.")
        print("남은 커피의 양은 %d개 입니다." % coffee)
    if coffee == 0:
        print("커피가 다 떨어졌습니다. 판매를 중지 합니다.")
        break
        
#list comprehension
# a에서 짝수만 3곱하기


a = [1,2,3,4]
>>> result = [num * 3 for num in a if num % 2 == 0]
>>> print(result)


# list comprehension 짝수곱만 표현되게 하기

result = [x*y for x in range(2,10,2)
...               for y in range(1,10)]
>>> print(result)
