# Multi-Agent Architectures

LangGraph를 사용한 멀티 에이전트 아키텍처 프로젝트입니다.

## 프로젝트 구조

- `supervisor_graph.py`: Supervisor 아키텍처 구현
- `network_graph.py`: Network 아키텍처 구현
- `langgraph.json`: LangGraph 설정 파일

## 실행 방법

원하는 `*.py` 파일을 실행하려면 다음 단계를 따르세요:

1. `langgraph.json` 파일을 실행하려는 파일에 맞게 수정합니다.

   예를 들어, `supervisor_graph.py`를 실행하려면:
   ```json
   {
     "dependencies": ["./supervisor_graph.py"],
     "graphs": {
       "agent": "./supervisor_graph.py:graph"
     },
     "env": ".env"
   }
   ```

   `network_graph.py`를 실행하려면:
   ```json
   {
     "dependencies": ["./network_graph.py"],
     "graphs": {
       "agent": "./network_graph.py:graph"
     },
     "env": ".env"
   }
   ```

2. LangGraph 개발 서버를 실행합니다:
   ```bash
   langgraph dev
   ```

## 주의사항

- 실행하려는 Python 파일에서 `graph` 객체를 export해야 합니다.
- `.env` 파일에 필요한 환경 변수(API 키 등)가 설정되어 있어야 합니다.
