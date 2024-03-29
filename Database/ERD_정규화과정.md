## ERD(Entity Relationship Diagram)
- 데이터베이스를 구축할때 가장 기초적인 뼈대 역할, 릴레이션간의 관계들을 정의한것.
### 중요성
- ERD는 시스템의 요구사항을 기반으로 작성되며, 이것을 기반으로 데이터베이스를 구축한다.
- 데이터베이스를 구축한 이후에도 디버깅 또는 비즈니스 프로세스 재설계가 필요한 경우에 설계도 역할을 담당하기도 한다.
- ERD는 관계형구조로 표현할수없는 데이터를 구성하는데 유용하지만 비정형데이터는 충분히 표현불가능


## 정규화과정
- 릴레이션간의 잘못된 종속 관계로 인해 데이터베이스 이상 현상이 일어나서 이를 해결하거나, 저장공간을 효율적으로 사용하기위해 릴레이션을 여러개로 분리하는 과정
- 데이터베이스 이상현상 : 회원이 한개의 등급을 가져야하는데 세 개의 등급을 갖거나 삭제할 때 필요한 데이터가 같이 삭제되고, 데이터를 삽입해야하는데 하나의 필드값이 null되면 안되어서 삽입하기 어려운현상
### 정규형원칙
- 정규형의 원칙이란 같은 의미를 표현하는 릴레이션이지만 좀 더 좋은 구조로 만들어야 하고, 자료의 중복성은 감소해야하고, 독립적인 관계는 별개의 릴레이션으로 표현해야하며, 각각의 릴레이션은 독립적인 표현이 가능해야 하는 것을 말합니다.
- 제 1정규형
  - 릴레이션의 모든 도메인이 더이상 분해될수없는 원자값만으로 구성되어야 합니다. 릴레이션의 속성 값 중에서 한개의 기본키에 대해 두개 이상의 값을 가지는 반복집합이 있어서는 안 됩니다. 만약에 반복집합이 있으면 제거해야한다.
- 제 2정규형
  - 릴레이션이 제 1정규형이며 부분함수의 종속성을 제거한 형태를 말함 부분함수의 종속성 제거란 기본키가 아닌 모든 속성이 기본키에 완전 함수 종속적인것을 말한다.
- 제 3정규형
  - 제 2정규형이고 기본키가 아닌 모든속성이 이행적함수종속을 만족하지 않는 상태를 말한다.
  - 이행적함수종속 : a -> b/b -> c가 존재하면 논리적으로 a -> c가 성립하는데, 이때 집합 c가 집합 a에 이행적으로 함수 종속이 되었다고 한다.
