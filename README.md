# KAKAO_MOBILITY_TEST


카카오 모빌리티 IOS 내비 과제

특정 좌표(x, y)를 입력받아, 좌표에 해당하는 ZONE의 명칭을 표출하는 ReverseGeocoder 모듈 및 앱을 구현하십시오.

=========================================================================================

zone 검색 속도를 높이기 위해서
파일읽기&데이터 파싱할때, 모든 zone과 polygon의 MBR 값을 만들었습니다. (zone의 MBR은 포함된 polygon을 이용하여 만들었습니다.)
검색순서는 mesh MBR -> zone MBR -> polygon MBR -> polygon. (입력한 x, y 값이 각각의 MBR안에 있을 경우 다음으로 진행)

polygon안에 x, y값이 있는지에 대한 판별은,

다각형 안에 일정 점에서 밖으로 나가는 선을 그어
교차되는 점의 갯수가 홀수이면 안에 있고,
짝수이면 밖에 있다고 판정.

입력한 x, y 좌표가 polygon 안에 있을 경우 해당 zone 출력.

=========================================================================================

일단, 결과값은 정확하다.

카카오 모빌리티에서 예제로 제공해준 검증값이 일치했고, 내가 검증 프로세스를 만들어 결과를 확인했다.

속도 문제도 아닌거 같다.

좌표 1개 평균 검색시간이 0.0029초 정도나오니, 속도 문제도 아닌거 같다.


이유가 뭘까.. 
  
1. 데이터 파싱과 검색부분을 Framework, library 형태로 안만들어서 그런건가?
  
---> 모듈(SDK, Framework, library)을 만들고 이를 이용한 샘플을 만들어 제출해라.  
이런식으로, 원하는 바를 좀더 명확하게 써줬으면 좋았을거 같다. 
  
2. MVVM 패턴으로 만들지 않아서 그런걸까?

3. 결과값이 다른걸까?

---> 일치하지 않는 무언가가 있는걸까?



이직하고 싶었던 회사였는데, 

기대를 많이 했었던 만큼 아쉬움도 크다.

더 좋은곳이 있겠지, 긍정적으로 생각하자. 



![IMG_3895](https://user-images.githubusercontent.com/5820255/74238177-9a35ea80-4d18-11ea-8563-16a9f7941a17.PNG)
