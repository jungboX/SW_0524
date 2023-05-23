# SW_0524
#### 명령어 `top`, `ps`, `jobs`, `kill` 알아보기
<br>

## *top*
**설명**
- 시스템 프로세스/메모리 사용 현황을 5초 간격으로 업데이트하여 출력
- 현재시간, 시스템 업데이트 시간, 시스템에 로그인한 사용자 수, 1, 5, 15분간의 시스템 평균 부하 출력

**사용법**
> top [옵션]

|옵션|설명|
|---|:---:|
|`-b`|배치모드로 정보를 출력. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력|
|`-d`|지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력|
|`-i`|토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않음|
|`-n`|지정한 시간(num)만큼 업데이트 정보를 출력|
|`-p`|지정한 프로세스 ID(pid)의 정보만을 출력|
|`-q`|시간의 간격 없이 계속하여 업데이트 정보를 출력|
|`-s`|몇 개의 대화식 명령을 비활성화(시큐어 모드)|
|`-S`|누적된 정보를 출력(cumulative 모드)|

실제 top명령어 실행 화면

![](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705212456131_V9D3Q4JJL.jpg/ka38_331_i1.jpg?type=w575_fst_n&wm=Y)

[top 자세히 알아보기](https://terms.naver.com/entry.naver?cid=59321&docId=4125861&categoryId=59321&expCategoryId=59321)
<br><br>

## *ps*
**설명**
- 프로세스의 현재 상태를 출력

**사용법**
> ps [옵션]

|옵션            |전체 프로세서와 관련된 옵션 설명|
|---             |:---:|
|`-A`            |모든 프로세스를 출력|
|`-N, --deselect`|-A 옵션과 비슷하나 ps 프로세스를 제외하고 출력|
|`-a`            |세션 리더 및 터미널에 속하지 않는 프로세스를 제외하고 출력|
|`-d`            |세션 리더를 제외한 모든 프로세스를 출력|
|`-e`            |커널 프로세스를 제외한 모든 프로세스를 출력|
|`T`             |현재 터미널에서의 모든 프로세스를 출력|
|`a`             |현재 터미널의 사용자 고유 프로세스를 출력|
|`r`             |현재 실행 중인 프로세스를 출력|
|`x`             |터미널이 없는 프로세스를 출력|

실제 ps 명령어 실행 화면

![](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705210350328_XVD2UXMLY.jpg/ka38_241_i1.jpg?type=w575_fst_n&wm=Y)

[ps 자세히 알아보기](https://terms.naver.com/entry.naver?cid=59321&docId=4125773&categoryId=59321)
<br><br>

## *jobs*
**설명**
- 현재 세션의 작업 상태 출력
- (*작업 중지된 상태*, *백그라운드로 진행 중인 작업 상태*, *변경 되었지만 보고 되지 않은 상태* 등)

**사용법**
> jobs [옵션] [job ID]

> jobs -x command [args]

|옵션     |설명|
|---      |:---:|
|`-l`     |프로세스 그룹 ID를 state 필드 앞에 출력|
|`-n`     |프로세스 그룹 중에 대표 프로세스 ID를 출력|
|`-p`     |각 프로세스 ID에 대해 한 행씩 출력|
|`command`|지정한 명령어를 실행|

실제 jobs 명령어 실행 화면

![](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170710154910976_RX87MMBQ3.jpg/ka38_149_i2.jpg?type=w575_fst_n&wm=Y)

[jobs 자세히 알아보기](https://terms.naver.com/entry.naver?cid=59321&docId=4125682&categoryId=59321&expCategoryId=59321) 
<br><br>

## *kill*
**설명**
- 프로세스에 종료 시그널을 보냄
- 문제가 생긴 프로세스 종료 가능

**사용법**
> kill [-s시그널] [-a] pid ···

> kill -l [시그널]

|옵션     |설명|
|---      |:---:|
|`pid ···`|종료시킬 프로세스 ID나 프로세스 이름을 지정|
|`-s`     |전달할 시그널의 종류를 지정, 이 위치에 시그널 이름이나 번호를 작성|
|`-l`     |시그널로 사용할 수 있는 시그널 이름들을 보여줌|
|`-1`     |-HUP 프로세스를 재활성화|
|`-9`     |프로세스를 강제로 종료|

실제 kill 명령어 실행 화면

![](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705204104854_AGTP0ICWJ.jpg/ka38_154_i3.jpg?type=w575_fst_n&wm=Y)

[kill 자세히 알아보기](https://terms.naver.com/entry.naver?cid=59321&docId=4125687&categoryId=59321&expCategoryId=59321) 

