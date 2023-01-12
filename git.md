# **GIT** 
분산 버전 관리 프로그램  (VCS)
*** 
- 코드의 히스토리 (버전)을 관리하는 도구
- 개발되어온 과정 파악 가능
- 이전 버전과의 변경 사항 비교 및 분석
---

<!-- 말로 풀자면,, 추가/수정/삭제에 의한 여러 버전이 생김-> 변경사항 & 최종본만 저장하는 도구가 git임. 즉 어떤 변경 사항이 있엇는지 대신 기록함. 변경사항 기준으로 프로그램 관리해주는 툴임. 소스코드가 변경된 이력을 쉽게 확인할 수 있음. <br> -->
<!-- git 은 분산버전관리가 가능하게 하는 프로그램이며,  github, gitlab은 저장소( 저장 서비스)임. -->
### **용어** 
    버전 = 컴퓨터 소프트웨어의 특정 상태  
    관리 = 어떤 일의 사무, 시설이나 물건의 유지/개량  
    프로그램 = 컴퓨터에서 실행될 때 특정 작업을 수행하는 일련의 명령어들의 모음 
    Git =  분산 버전 관리 프로그램
    Github or Gitlab = Git 기반의 저장소 서비스
### **GUI & CLI**
```PYTHON
GUI = graphic user interface
그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식  ex. 마우스   
CLI = Command Line interface
명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식  ex. 키보드, 본체  
```
- GUI 는 CLI 에 비해 사용하기 쉽지만 단계가 많고 컴퓨터의 성능을 더 많이 소모함.  
- 수많은 서버/개발 시스템이 CLI를 통한 조작 환경을 제공. (훨씬 더 적은 리소스 소모.)

### CLI 예시
--- 
<br> Git bash 실행 후 git 실행한 결과  
`command = git`
![git 실행화면](git/1.png)  

<br> 현재 폴더에 어떤 파일 있는지, 내용물 보여주는 거임.  
ls=list  
`command = ls`
![git 실행화면](git/2.png)  
 
 <br> 현재 위치 변경.
 cd=change directory  
`command = cd Desktop`
![git 실행화면](git/3.png)  

이후 `ls` 입력시 바탕화면 파일들 확인 가넝  
이후 `cd m` 입력시 m 폴더로 위치이동
`ls` 로 m 내에 있는 파일 확인 가능

![](git/4.png) 

<br> 상위 폴더로 이동.   
`command = ..`
![git 실행화면](git/5.png)  

<br> 현재 위치 폴더 내 파일 생성.   
`command = touch 파일명.확장자`
![git 실행화면](git/6.png)  
![git 실행화면](git/6_2.png)  

<br> 현재 위치 폴더 내 폴더 생성.   
`command = mkdir 폴더명.확장자`
![git 실행화면](git/7.png)  

<br> 현재 위치 파일 삭제.   
`command = rm 파일명.확장자`
![git 실행화면](git/8.png)  

<br> 현재 위치 폴더 삭제. 휴지통에 안보냄;   
`command = rm -r 폴더명.확장자`
![git 실행화면](git/9.png)  

<br> 오류문구에서 왜 오류났는지는 다 말해주기 때문에 읽으면 극복 가능함 ㅇㅇ.   
![git 실행화면](git/10.png)  

<br> 현재 위치의 파일 탐색기 실행.   
`command = explorer`

```
sudo rm -rf /
sudo : 관리자 권한으로 
rm : 지워라 
-r : 폴더 
f : 강제로 
/ : 컴퓨터의 가장 최상위 폴더임; c 드라이브
```   

1. 절대경로
- 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것 
- 윈도우 바탕 화면의 절대 경로 = `C:/Users/ssafy/Desktop`
2. 상대경로
- 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것. 
- 현재 작업하고 있는 디렉토리가 `C:/Users` 일 때 윈도우 바탕 화면으로의 상대 경로는 `ssafy/Desktop`
- `./` 현재 작업하고 있는 폴더  `../` 현재 작업하고 있는 폴더의 부모 폴더

<br> 현재 위치 표시.   
`command = pwd`
<br> 위치 이동시 절대경로로 입력해도 됨.   
`command = cd /c/Users/SSAFY/Desktop/m/image`

---

폴더 생성
VScode 로 열기- ctrl+shit+p terminal: create new terminal 하고 환경 hit bash로 바꿔주면 git bash랑 기능적으로 똑같게 됨.  
Git 은 repository 라는 저장소 이용  
git init 으로 저장소 생성
VScode 에서 함  
이 파일을 버전 관리하며 git을 사용한다 = 특정 버전으로 남긴다 = 커밋(Commit)한다  
-> 3가지 영역을 바탕으로 동작함. 
```
readme.md 생성
teminal 에 git init 입력 : 비어있는 GIT 저장소를 만들었따
해당 폴더는  git 으로 관리되는 폴더다~ ㅇㅎㅇㅎ 보기-숨긴항목 해야 보임
-> (master) 
-> git add readme.md 로 추가함. 
git commit -m "add readme.md"  놨더니 오류 뜸
```
![](git/11.png)  
이메일, 닉네임 추가하고 커밋했더니 되넹 ㅇㅇ
![](git/13.png)  

```python
git add
git commit -m "수정하는 이유"
git status : 
```

![](git/14.png)  
![](git/15.png)  

**오류정리**
```
git commit 이라고만 치면 오류뜸; 
왜 수정하는지 이유 없어서임 
그럴때 아래 명령어로 exit 
:q!
-> Aborting commit due to empty commit message.
라고 git 이 응답함. 이유 안말해주니 커밋 안하겠다는 뜻임.
```
```
git log 모든 이력을 한 화면에 나타내지 못해서 입력 불가인 오류 뜸; 
아래 명령어로 exit 
q
```

github 에서 프로젝트 시작해서 수정하는 것도 함!  
repositury 생성-  
git bash에 command 입력 - 여러 개발자가 자기 폴더에 복제 가능함 ㅇㅇ 저장소도 public으로 설정해놨기 떄문에~
```
git clone https://github.com/juyeon-kimm/TIL.git 
```
그럼 폴더 생김 폴더 내에서 VScode 로 열기로 실행함  
입력-add-commit-
git push 해서 git hub 에 올림  -> 브라우저 로그인하라는 창 뜸

![](git/17.png)

github 명령어 정리
![](git/16.png)  

커밋 이력 남기기 전에 pull하면 됨.
