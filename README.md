# pratice

# 자판기 파이썬 코드
# 600원이상 돈을 넣어야지 메뉴 선택이 가능함
print('='*46)
print('='*15,'----자판기----','='*15)
print('='*46)
print('==','1.콜라','==','2.사이다','==','3.물','='*5,'insert','='*3)
print('==','-'*6,'==','-'*8,'==','-'*4,'='*5,'------','='*3)
print('==','  600 ','==','   800  ','==','1000','='*5,' 000원','='*3)
print('='*35,'------','='*3)
print('==','+'*40,'==')
print('==','+'*40,'==')
print('==','+'*40,'==')
print('==','+'*14,' '*10,'+'*14,'==')
print('==','+'*14,' '*1,'SMHRD',' '*2,'+'*14,'==')
print('==','+'*14,' '*10,'+'*14,'==')
print('==','+'*40,'==')
print('==','+'*40,'==')
print('='*46)
print('='*46)
print(' '*2,'='*3,' '*32,'='*3,' ')
print(' '*2,'='*3,' '*32,'='*3,' \n')

insert_coin = int(input("insert coin >> "))
if insert_coin < 600:
    print(f"돈을 더 넣어주세요({600-insert_coin}원 부족)")
else:
    select_menu = int(input("select menu >> "))
    if select_menu == 1:
        if 600 > insert_coin:
            print("금액 부족")
        else:
            balance = insert_coin - 600
            print(f"잔돈 >> 1000원 {balance//1000}개, 500원 {balance%1000//500}개, 100원 {balance%1000%500//100}개")
            
    elif select_menu == 2:
        if 800 > insert_coin:
            print("금액 부족")
        else:
            balance = insert_coin - 800
            print(f"잔돈 >> 1000원 {balance//1000}개, 500원 {balance%1000//500}개, 100원 {balance%1000%500//100}개")
            
    elif select_menu == 3:
        if 1000 > insert_coin:
            print("금액 부족")
        else:
            balance = insert_coin - 1000
            print(f"잔돈 >> 1000원 {balance//1000}개, 500원 {balance%1000//500}개, 100원 {balance%1000%500//100}개")
            
    else :
        print("잘못된 메뉴 선택")
