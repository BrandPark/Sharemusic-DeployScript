# Sharemusic-DeployScript
코드를 pull하고 `npm`을 통해 의존성이 등록된 라이브러리들을 다운 받아 배포까지 하는 스크립트입니다.

Travis-CI를 사용하면서 현재는 사용하지 않습니다.

## 수행 명령
1. git pull 을 통해 코드 최신화
2. npm install 을 통해 package.json 에 등록된 의존성들을 다운받는다.
3. ./gradlew build 를 통해 빌드 한다.
4. 생성된 .jar 파일을 루트 디렉터리로 복사한다. 
5. 애플리케이션이 구동 중인지 확인하여 종료시킨다.
6. nohup 를 통해 백 그라운드로 .jar 파일을 실행한다.
   - 이때 스프링 vm 설정으로 실행에 필요한 active profile과 설정파일들을 옵션으로 한다.
