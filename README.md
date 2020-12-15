# MarineWiz 2.0
MarineWiz는 발주자의 다양한 요구사항을 반영한 고품질 SW를 저렴한 비용으로 빠르게 개발 가능한 조선해양특화 SW통합개발도구
V2.0 : 
  - MVVM 기반의 개발 방법론의 적용 범위 확장 : 사용자 GUI 컴포넌트 지원, 외부 라이브러리 연동, 템플릿 기능
  - Android 및 iOS 개발 환경 지원

***

## [목 차]
1. [개요](#개요)
2. [설치 방법 및 환경 설정](#설치-방법-및-환경-설정)
3. [사용 방법](#사용-방법)

***

## [개요]
### 1. 재사용 가능한 템플릿 기반의 빠른 프로토타이핑 개발 지원
- DRAG & DROP 방식의 컴포넌트기반 템플릿을 활용하여 조선해양 SW의 프로토타입을 빠르고 편리하게 개발 가능
### 2. 비지니스 로직과 UI 분리를 통한 재사용 구조화로 반복적인 개발 최소화
- 사용자 요구사항을 재사용 가능한 UI와 비지니스 로직으로 분리하여 유사한 종류의 SW를 저렴한 비용으로 재사용 가능하게 개발하는 방법 지원
### 3. 적용 분야
- 조선해양 중소.중견기업의 SW개발, 선박 기자재 탑재용 SW개발, 비숙련 개발장 교육, 관련 학과의 인력 양성 등에 적용 가능

![marinewiz](https://user-images.githubusercontent.com/45934727/73902010-d95ada80-48d7-11ea-91dc-cea54f775ec3.JPG)

## [설치 방법 및 환경 설정]
### 1. 설치 방법
* 다운로드
   -  MarineWiz 설치파일, 필수 설치 디렉토리의 파일을 모두 다운받는다.
   -  NDP472-DevPack-ENU.exe 를 설치한다.
   -  setup.exe 를 실행한다.

### 2. 환경 설정
- MSBuild를 기반으로 Build를 수행하여야 하기 때문에 MSBuild 경로를 설정해야 한다.
   - Main 화면의 상단 Menu Project > Option > Build Tab에 경로 설정한다.
	
## [사용 방법]
### MarineWiz 기반 SW개발
1. 프로젝트 생성
  - 프로젝트 생성 화면에서 제작하고자 하는 응용프로그램의 템플릿을 선택한다.프로젝트 생성 화면은 MarineWiz를 실행하거나, 메뉴바에서 「File > New Project」를 선택했을 때 출력된다.
  - 프로젝트의 이름과 저장 위치(기본 : C:\Users\Name\Desktop)를 설정한 후 OK 버튼을 클릭한다. 저장 위치를 변경할 경우 Find버튼을 클릭한다.
  
![image01](https://user-images.githubusercontent.com/45934727/77042216-a50e2a00-69fe-11ea-920f-5a6c7fdbb129.png)
  - 프로젝트 생성 화면에서 설정한 값(프로젝트 이름, 저장 위치)을 확인한다.
  - 프로젝트에서 제작하려는 응용프로그램 메인화면의 너비와 높이를 설정한 후 OK버튼을 클릭하여 프로젝트 정보를 저장한다. CANCEL 클릭하면 설정한 너비와 높이를 무시하고 기본 크기(1000 * 60)로 프로젝트 정보가 저장된다.
![image](https://user-images.githubusercontent.com/45934727/77055550-6edba500-6a14-11ea-9e7b-7e38d08a79f4.png)
   
2. 응용 프로그램 구성
  - 프로젝트 작업 화면에서 컴포넌트 목록창의 컴포넌트를 Drag & Drop하여 응용프로그램의 GUI를 구성한다.
  - 응용프로그램의 GUI를 구성하는 컴포넌트를 선택하여 속성 값을 설정한다.
  
![image](https://user-images.githubusercontent.com/45934727/77055672-a9454200-6a14-11ea-88eb-19e05e1f0976.png)

3. 데이터 바인딩
  - 메뉴바에서 「File > Add Library(DLL) Files」를 클릭해서 프로젝트에 필요한 DLL을 Import한다. Import된 DLL은 솔루션 탐색기의 package폴더에 저장된다.
  
![image](https://user-images.githubusercontent.com/45934727/77056032-34263c80-6a15-11ea-9bba-a1233b191798.png)
  - 데이터를 바인딩하기 위한 컴포넌트를 선택한 후 오른쪽 마우스 버튼을 클릭하여 「Attached Data From...」을 클릭한다.

![image](https://user-images.githubusercontent.com/45934727/77056186-6fc10680-6a15-11ea-8f49-90ffa1928e60.png)
  - DLL을 선택한다.
  - 내부 함수를 선택한다. 『class DatabaseAccessManager > List<double> GetDataFrom()』 선택
  - 「Next」 버튼을 클릭한다.

![image](https://user-images.githubusercontent.com/45934727/77056309-954e1000-6a15-11ea-8f85-7208fe3c8c97.png)
  - 데이터 바인딩 대상 컴포넌트, 선택한 DLL 파일, 내부 함수를 확인한다.
  - 바인딩 데이터의 갱신 주기를 설정한다.
  - 차트 컴포넌트의 데이터 범위를 설정한다.
  - 「Finish」버튼을 클릭한다.

![image](https://user-images.githubusercontent.com/45934727/77056440-be6ea080-6a15-11ea-9187-7e3a48ec34bf.png)

4. 저장
  - 메뉴바에서 「File > Save」을 클릭한다.
  - 메뉴바에서 「Build > Build(B)」를 클릭한다.
  - Console화면이 생성되고, Build 정보가 출력된다.
  - Build가 완료되면 「프로젝트 저장위치\Bin\Debug」폴더에 exe 파일이 생성된다.

![image](https://user-images.githubusercontent.com/45934727/77057819-dfd08c00-6a17-11ea-86b5-9f278f5c9969.png)
 
5. Build
  - 메뉴바에서 「Build > Build(B)」를 클릭한다.
  - Console화면이 생성되고, Build 정보가 출력된다.
  - Build가 완료되면 「프로젝트 저장위치\Bin\Debug」폴더에 exe 파일이 생성된다.

![image](https://user-images.githubusercontent.com/45934727/77056699-245b2800-6a16-11ea-9154-4ce05f777bd8.png)
      
6. 응용 프로그램 실행
  - 「프로젝트명.exe」을 더블클릭하여 실행시키면 응용프로그램의 동작을 확인할 수 있다.

![image](https://user-images.githubusercontent.com/45934727/77056981-9895cb80-6a16-11ea-9e17-efd552dc51e2.png)
