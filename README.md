### 순서
### git
### 최초세팅

```bash
git clone [저장소 URL]
#의존성 설치
npm install

Docker 설치
#Docker 컨테이너 빌드 및 실행
docker-compose up --build
```


### git 협업방법
```bash
#최신 변경사항 가져오기
git pull origin main
### 본인이 담당한 기능개발 브랜치 생성
git checkout -b feature/new-feature
개발하기
개발완료하고 실행하기
#도커 사용시
docker-compose up
#컨테이너 종료
docker-compose down
#도커 사용 안할시
npm start
#리액트 종료
터미널에서 Ctrl+C

코드 테스트 및 재검토
#변경사항 스테이징
git add .
git commit -m "커밋메세지"
git push origin feature/new-feature


```
### 동료가 코드 리뷰및 테스트
다른 팀원들이 Pull Request 리뷰

피드백 하고 Pull Request 승인 및 거부

Pull Request 승인하면 main 브랜치로 병합



```bash
#메인 브랜치에 병합
git checkout main
git pull origin main

git merge feature/new-feature
git push origin main
```
### 배포(중요 진행이 완료되었을 때)
```bash
#도커 허브 또는 기타 레지스트리에 이미지를 푸시
docker build -t your-username/your-repository:tag .
docker push your-username/your-repository:tag
#서버에서 도커 이미지를 풀하고 컨테이너를 실행
docker pull your-username/your-repository:tag
docker run -d -p 80:3000 your-username/your-repository:tag

```



