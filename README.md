# 동국대학교 통계학과 빅데이터 분석 학회 비어플
## Dongguk Univ. B.A.F
### 첫 번째 프로젝트 - 마키아벨리즘 테스트 응답을 통한 투표 여부 예측

**Data**
* train.csv - 45,532 rows and 78 cols(include "voted" column)
* test.csv - 11,382 rows and 77 cols(not include voted column)  

**Columns**
|Name|Type|Information|Example|
|:--:|:--:|:---------:|:-----:|
|index|int|인덱스|0, 1, 2, 3, 4, 5, 6, 7, ...|
|Q_A(a~t)|num|마키아벨리즘 테스트 문항 별 점수|3, 5, 4, 3, 1, ...|
|Q_E(a~t)|int|마키아벨리즘 테스트 문항 별 응답 시간, 상대적 시간, 20개|363, 647, 1623, 504, 927, ...|
|tp__(01~07)|int|5가지 성격 요소 파악을 위한 10 항목 검사 문항, 10개|2, 1, 2, 2, 1, 5, ...|
|wr_00(01~13)|int|실존 단어의 뜻을 아는지에 대한 응답|1, 1, 1, 0, 1, 0, ...|
|wf_00(01~03)|int|허구 단어의 뜻을 아는지에 대한 응답|0, 0, 0, 0, 1, 0, ...|
|age_group|chr|연령, 10대 ~ 70대 이상|30s, 20s, 30s, 20s, ...|
|education|int|교육 수준|2, 4, 3, 4, 3, 2, ...|
|engnat|int|모국어 영어 여부|1, 2, 1, 2, 1, 1, ...|
|familysize|int|형제 자매 수|4, 3, 3, 0, 2, 6, 3, ...|
|gender|chr|성별|Female, Female, Male, Female, ...|
|hand|int|주로 사용하는 손|1, 1, 1, 1, 2, 1, 1, ...|
|married|int|혼인 상태|3, 1, 2, 1, 2, 3, 1, ...|
|race|chr|인종|White, Asian, White, Asian, ...|
|religion|chr|종교|Other, Hindu, Other, Hindu, ...|
|urban|int|유년기 거주 구역|1, 3, 2, 3, 1, 2, 2, 2, 1, ...|
|voted|int|지난 해 국가 선거 투표 여부|2, 2, 1, 1, 1, 2, 1, 1, 1, 1, ...|

**Columns Characteristic**
- age_group  
  - 1 : Less than high school  
  - 2 : High school  
  - 3 : University degree  
  - 4 : Graduate degree  
  - 0 : No answer  
- engnat
  - 1 : Yes  
  - 2 : No  
- hand  
  - 1 : Right  
  - 2 : Left  
  - 3 : Both  
  - 0 : No answer  
- married  
  - 1 : Never married  
  - 2 : Currently married  
  - 3 : Previously married  
  - 0 : Other(NA etc.)
- race  
  - Asian, Arab, Black, Indigenous Australian, Native American, White, Other
- religion  
  - Agnostic, Atheist, Buddhist, Christian_Catholic, Christian_Mormon, Christian_Protestant, Christian_Other, Hindu, Jewish, Muslim, Sikh, Other
- urban
  - 1 : Rural(country side)
  - 2 : Suburban
  - 3 : Urban(town, city)
  - 0 : No answer
- Q_A : 비식별화를 위해 일부 질문은 Secret  
  - Qa : Secret
  - Qb : The biggest difference between most criminals and other people is that the criminals are stupid enough to get caught.
  - Qc : Anyone who completely trusts anyone else is asking for trouble.
  - Qd : Secret
  - Qe : P.T. Barnum was wrong when he said that there's a sucker born every minute.
  - Qf : There is no excuse for lying to someone else.
  - Qg : Secret
  - Qh : Most people forget more easily the death of their parents than the loss of their property.
  - Qi : Secret
  - Qj : It is safest to assume that all people have a vicious streak and it will come out when they are given a chance.
  - Qk : All in all, it is better to be humble and honest than to be important and dishonest.
  - Ql : Secret
  - Qm : It is hard to get ahead without cutting corners here and there.
  - Qn : Secret
  - Qo : The best way to handle people is to tell them what they want to hear.
  - Qp : Secret
  - Qq : Most people are basically good and kind.
  - Qr : One should take action only when sure it is morally right.
  - Qs : It is wise to flatter important people.
  - Qt : Secret
    - 1 : Disagree
    - 2 : Slightly disagree
    - 3 : Neutral
    - 4 : Slightly agree
    - 5 : Agree
- tp__(01~07) : items were rated "I see my self as:" _____ such that
  - tp01 : Extraverted, enthusiastic.
  - tp02 : Critical, quarrelsome.
  - tp03 : Dependable, self-disciplined.
  - tp04 : Anxious, easily upset.
  - tp05 : Open to new experiences, complex.
  - tp06 : Reserved, quiet.
  - tp07 : Sympathetic, warm.
  - tp08 : Disorganized, careless.
  - tp09 : Calm, emotionally stable.
  - tp10 : Conventional, uncreative.
    - 7 : No answer
    - 6 : Disagree strongly
    - 5 : Disagree moderately
    - 4 : Disagree a little
    - 3 : Neither agree nor disagree
    - 2 : Agree a little
    - 1 : Agree moderately
    - 0 : Agree strongly
- wr_00 & wf_00
  - boat, incoherent, pallid, robot, audible, *cuivocal*, paucity, epistemology, *florted*, decide, pastiche, *verdid*, abysmal, lucid, betray, funny
  - 1 : Yes
  - 0 : No
- voted
  - 1 : Yes
  - 2 : No
    
    
    
    
    
    
    
