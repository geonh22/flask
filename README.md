# [EPC monitoring]
EPC 서비스 이상징후 점검을 위한 Cloud 인프라 점검 자동화  

- VM, VR, Cnode 의 CPU, mem 분석   
- LB, Storage, NW 분석  

## 기본 setting 


python -m venv venv  
source venv/Scripts/activate  
python -m pip install --upgrade pip  
pip install -r requirements.txt  
python run.py  

internet => 127.0.0.1 조회 

## 현재 진행 상황 

template  
- index.html ( 날짜 선택 page )  
- **_start.html ( 각 인프라 최근 사용량 출력 --> 기간 선택 시, lookup.html로 이동 )  
- **_lookup.html ( 각 인프라 기간 별 조회 )  

common  
- navbar.html  : 사이드 네비 바 관련 html 파일    

run.py  ( flask 실행 파일 )   
cal.py ( calday : 기간 내 db 조회 / caltotal : 오늘의 total 인프라 갯수 조회)   
datepick.py (  )   
search.py  ( 조회할 인프라 찾아서 오늘 data 조회, db 이름: 인프라명/ table 이름: 개체명 )