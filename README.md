# java-lotto-precourse
## 프로그램  
간단한 로또 발매기

- 입력
  1. 사용자로부터 1000원 단위로 구입 금액을 입력받는다.
  2. 당첨번호(번호는 쉼표를 기준으로 구분) 6개와 보너스 번호 1개를 입력받는다. 

- 출력
  1. 사용자가 입력한 구입 금액한에서 로또를 구입해 출력한다. (각각의 로또 수량 및 번호를 출력, 이때 로또 번호는 오름차순으로 보여준다.)
  2. 당첨 내역 및 수익률을 출력한다. (수익률은 소수점 둘째 자리에서 반올림)
     
- 로직  
  1. 로또 번호 검사 (1~45번까지만 유효한 로또 번호)
  2. 로또 번호 발행 (중복되지 않는 숫자 6개 + 보너스 번호 1개 )
  3. 당첨 1등부터 5등까지 선정
  4. 수익률 계산
-----
    당첨 기준과 금액
    1등: 6개 번호 일치 / 2,000,000,000원
    2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    3등: 5개 번호 일치 / 1,500,000원
    4등: 4개 번호 일치 / 50,000원
    5등: 3개 번호 일치 / 5,000원

## 예외처리
- 입력
  1. 사용자가 1000원 단위로 구입 금액을 입력하지 않은 경우
  2. 사용자가 금액을 숫자로 입력하지 않고 알파벳이나 한글, 특수문자등을 입력한 경우 
  3. 사용자가 당첨번호를 6개를 다 입력하지 않고 더 많이 입력하거나 적게 입력한 경우 
  4. 사용자가 당첨번호를 쉼표로 구분하지 않고 다른 특수 문자로 구분한 경우
  5. 사용자가 쉼표로 구분을 했지만 쉼표가 연속되게 나오는 경우
  6. 당첨번호 혹은 보너스 번호에 숫자가 아닌 알파벳이나 한글, 특수문자등을 입력한 경우
  7. 당첨번호 혹은 보너스 번호에 숫자 범위(1~45)를 넘기는 수가 포함된 경우
  8. 사용자가 빈문자열만 입력한 경우
  
  -> 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받기  
  Exception이 아닌 IllegalArgumentException, IllegalStateException 등과 같은 명확한 유형을 처리

## 목표
-  한 기능을 하나의 메서드로 최대한 구분하기(길이가 길어지지 않게)
-  상수화 잊지말고 해주기
-  구현 순서 잘지키기(상수 or 클래스 변수 -> 인스턴스 변수 -> 생성자 -> 메서드)
-  테스트는 단위 테스트로 구현하기
-  필드는 private로 getter함수로 받아오기
-  최대한 순수함수로 구현(외부 상태에 영향이 없도록)
-  저번주보다 많이 늘기 🌱
     
