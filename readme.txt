# 구조
/
    L requirements.txt : 특정 환경에서 사용한 모듈을 기술
                         환경이 구축될때, 이 서비스 운영/개발 시 필요한 모듈 설치
                         하기 위해 기술되는 파일이다.
                         - 반드시 버전을 명시하여, 향후에 서버가 변경돼도, 문제없이
                            구동되겠금 동일한 환경을 제공     
    L run.py            : 서비스 메인
    L wsgi.py           : 엔트리포인트, 아파치서버가 바라보는 파일이다.
    L deploy.json       : 페브릭이 배포작업을 하는데 필요한 상수값들을 저장한 파일이다
                         - 환경변수가 저장된 파일

# fabric 설치
- pip(or conda) install fabric (결국 설치 불가~)
  => python2.7.xx 버전에 맞게 설치가 된다
  => python3.x 버전을 사용 불가 
- pip(or conda) install fabric3(o)

#에러체크
- 리눅스상에서
- $ tail -f /var/log/apach2/error.log
- 위의 명령어를 실행하고, 모니터링하면서, 문제점을 찾아서 수행
- 수정--> git에 반영 -> $ fab deploy

#github 사용
1. github.com 접속 후 저장소 생성
2. 로컬 PC에서 git 명령어를 이용하여 적절한 위치에 저장소를 다운로드