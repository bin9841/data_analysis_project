# Data Analysis

1. 데이터 전처리
    1. 파생변수 생성
        1. mach_score
            - 각 문항마다 점수가 그대로 들어가거나 역으로 계산되며 역으로 계산되는 문항의 점수 값을 반전시키고 상관분석을 통해 secret 처리 된 문항의 점수 값을 파악하여 점수 값을 반전시킴
        2. O C E A N
            - tipi 항목 검사를 통해 5가지 성격 특성요소에 관한 변수 5개 생성
        3. wr_mean, wf_mean
            - 실존/허구 단어에 대한 응답 평균 변수
        4. tactic, views, morality
            - Q_A 변수의 질문 특성에 따른 평균 변수
        5. qe_mean
            - QaE ~ QtE 까지의 시간 변수의 응답자별 평균 변수
    2. 재범주화
        1. age_group
            - 70대 이상의 빈도수가 적고 60대와 70대의 mach_score 등 수치형 변수들과의 관계에서 큰 차이가 없어 두 범주를 병합
        2. religion
            - mach_score 등의 수치형 변수들과의 관계에서 큰 차이가 없어 christian 관련 4가지 종교 병합 여부, 개체수가 적은 종교와 other 병합 여부 총 두 가지의 경우를 모두 관찰
        3. race
            - arab, indigenous australian, native american 의 빈도수가 적고 수치형 변수들과의 관계에서 큰 차이가 없어 black의 other로의 병합 여부에 따른 성능 비교 관찰
    3. 이상치 및 결측치 처리
        1. familysize
            - 16명 이상인 행 제거(percentile 0.995까지 사용)
        2. engnat, hand, married, urban
            - 무응답을 최빈값으로 대체
        3. tp##
            - 무응답을 중앙값으로 대체
        4. age_group & education
            - 10대 무응답 인원 및 학/석사 인원을 중졸:고졸비율로 수정
            - 나머지 그룹의 무응답 인원은 최빈값으로 대체
        5. 시간 변수
            - 이상치를 중위수로 대체
