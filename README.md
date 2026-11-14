# BOSUN WEB 포트폴리오

4인 캡스톤 프로젝트 **BOSUN**에서 WEB(채팅 화면 + WEB 백엔드)을 맡아 설계하고 만든 과정을 정리한 페이지입니다.

- **포트폴리오 페이지**: https://rlawlsy.github.io/2026-capstone-bosun-agent/
- **코드(팀 저장소)**: https://github.com/bosun-agent/bosun-agent

이 저장소에는 포트폴리오 페이지(`index.html`)와 화면 캡처(`img/`)만 있습니다. 코드는 팀 저장소에 있습니다.

## BOSUN

"web 컨테이너 재시작해줘" 같은 자연어로 Docker를 관리하는 서비스입니다. LLM이 쓸 도구를 정하고, Docker Agent가 Portainer를 거쳐 Docker를 조작합니다. 실제 실행 여부는 LLM이 아니라 정책(코드)과 사용자 승인이 정합니다.

## 맡은 부분

- **채팅 화면**: 정책이 "묻기"로 판정한 작업을 승인 카드로 보여 주고, 막힌 작업은 사유와 함께 안내
- **WEB 백엔드**: Agent 스트림 중계, 승인 만료·중복 처리, 감사 기록, Agent 실행 관리
- **정책 보드**: 작업을 허용·묻기·거부 칸으로 옮겨 Agent 설정에 저장
- **설치**: 첫 실행 설정 페이지, 웹과 Agent를 한 이미지로 묶은 컨테이너 설치

React 19 · TypeScript · Vite · Tailwind CSS · Node 22 · Hono · SQLite · Docker
