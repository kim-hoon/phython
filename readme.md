GIT HUB
ssh: git@github.com:kim-hoon/phython.git

1. git add . -> git commit 해서 우선 master branch로 변경 사항들을 다 커밋해준다.
2. git branch -m master main 명령어로 master 브랜치 이름을 main으로 변경해준다.
3. git status 로 아래의 메시지가 떠서 브랜치가 main으로 변경되어있는지를 확인해준다.
4. 그리고는 2번 단계에서 진행한 커밋단계를 main 브랜치로 push 해준다.
 git push -u origin main
5. 그리고 master 브랜치를 삭제해준다.
 git push origin --delete master


비밀번호없이 처리하는 방법 => https://goddaehee.tistory.com/254
1. ls -al ~/.ssh
2. 디렉토리가 없는경우 :   mkdir ~/.ssh => chmod 700 ~/.ssh => cd ~/.ssh
3. ssh keygen 생성 : sh-keygen -t rsa -b 4096 -C "yourEmail@example.com"


5.1) authorized_keys
 - id_rsa.pub 키의 값을 저장 한다.
5.2) id_rsa
 - 개인키, 타인에게 노출되면 안되는 private key 이다. 본인의 컴퓨터 내부에 저장하게 되어 있으며, 이 Private Key를 통해 암호화된 메시지를 복호화 할 수 있다.
5.3) id_rsa.pub
 - public key, 공개되어도 비교적 안전한 Key이다. Public Key를 통해 메시지를 전송하기 전 암호화를 하게 된다.
 - Public Key로는 복호화는 불가능 하다.
 - 접속하려는 Remote Machine의 authorized_keys에 입력하여 사용한다.
 6) ssh-agent 실행 여부 확인
  - ssh-agent가 정상 실행중인지 확인 해본다.
  - “Agent pid xxxxx” 과 같은 문장이 출력된다면 정상적으로 실행 중이다.
 # eval "$(ssh-agent -s)"

 


