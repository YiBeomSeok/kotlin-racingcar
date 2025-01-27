# kotlin-racingcar

## 초간단 자동차 경주 게임

1. 각 자동차에 이름을 부여합니다. 자동차 이름은 5자를 초과할 수 없습니다.

2. 전진하는 자동차를 출력할 때에는 이름을 같이 출력합니다.

3. 자동차 이름은 쉼표(,)를 기준으로 구분합니다.

4. 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려줍니다. 우승자는 한 명 이상일 수 있습니다.

```
경주할 자동차 이름을 입력하세요(이름은 쉼표(,)를 기준으로 구분).
pobi,crong,honux
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
crong : -
honux : -

pobi : --
crong : -
honux : --

pobi : ---
crong : --
honux : ---

pobi : ----
crong : ---
honux : ----

pobi : -----
crong : ----
honux : -----

pobi, honux가 최종 우승했습니다.
```

## 사전 구현 계획

- [x] 위치 - `Position`
- [x] 자동차 - `Car`
- [x] 자동차의 이동 정책 - `MovementPolicy`
- [x] 자동차들의 상태들을 관리 - `RacingCarRoad`
- [x] 우승자를 결정하는 정책 - `RankingPolicy`
- [x] 자동차에 이름을 부여할 수 있고 이름은 5자를 초과할 수 없다.
- [x] UI 로직: 자동차 이름은 쉼표로 구분한다.
- [x] 들여쓰기가 3 이상인 경우가 있다면 리펙토링한다.


- [x] `Car` 객체의 함수명 변경, 제약 조건 상수화
- [x] `RacingCarRoad`에 해당하는 에러 메세지는 `RacingCarRoad`가 관리한다.
- [x] `List<Car>`를 래핑한 일급 컬렉션을 사용한다.
  - [x] `RacingCarRoad`의 함수명에서 getXXX 형식을 버린다.
- [x] 사용하지 않는 함수는 삭제