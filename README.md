### auto commit 프로젝트

- 잔디밭관리용

----

- `git init` 먼저 하고 Default 레파지토리 만들기
- `Remote` 등록하기
- 배치파일 실행
  - `make file.exe`  실행
  - YYMMDD.md 파일 만들기
- git 명령어 순차 실행

---

- 배치파일 구체적인 내용

  - `make file.exe` 실행

  - git pull origin master

  - git add `YYMMDD.md`

  - git commit -m "na"

  - git push origin master

    - 다른사람이 했던 예제
    - GitAutoPush.bat

    ```python
    :loop
    	:: Navigate to the directory you wish to push to GitHub
    	::Change <path> as needed. Eg. C:\Users\pookie\Desktop\Writings
    	cd C:\Users\jhpark\Documents\GitHub\Docker
    
    	::Initialize GitHub
    	git init
    	
    	::Pull any external changes (maybe you deleted a file from your repo?)
    	git pull
    	
    	::Add all files in the directory
    	git add --all
    	
    	::Commit all changes with the message "auto push". 
    	::Change as needed.
    	git commit -m "auto push"
    	
    	::Push all changes to GitHub 
    	git push
    	
    	::Alert user to script completion and relaunch.
    	echo Complete. Relaunching...
    	
    	::Wait 3600 seconds until going to the start of the loop.
    	::Change as needed.
    	TIMEOUT 3600
    	
    ::Restart from the top.	
    goto loop
    ```