### 워크샵 아키텍처 ###
* 두뇌 (App): LangGraph (멀티 에이전트 및 루프 로직)
* 입구 (Serving): LangServe (FastAPI) (REST API 및 Playground 제공)
* 그릇 (Infra): Amazon EC2 + Golden Image (Packer) + Warm Pools
* 기억 (Persistence): Amazon DynamoDB (인스턴스가 교체되어도 대화 유지)
* 추론 (LLM): Amazon Bedrock (IAM Role을 통한 보안 연결

### 커리큘럼 (4~6시간 코스) ###
#### Module 1: LangGraph 기초 및 로컬 실습 ####
* LangGraph의 핵심 개념(Nodes, Edges, State) 이해하기.
* 간단한 검색 도구(Search Tool)를 사용하는 ReAct 에이전트 코드 작성.
* MemorySaver를 이용한 로컬 대화 기억 구현.

#### Module 2: EC2 인프라 구축 및 최적화 ####
* Amazon EC2 시작 템플릿 작성.
* Packer를 활용하여 의존성 라이브러리가 포함된 Golden Image 빌드.
* Warm Pools 설정으로 트래픽 급증 시 30초 이내 스케일링 대응 실습.

#### Module 3: LangServe & Bedrock 연동 ####
* LangServe를 사용하여 LangGraph를 웹 API로 변환.
* EC2에 IAM Role을 부여하여 Access Key 없이 Amazon Bedrock 호출하기.
* /playground를 통해 웹 환경에서 스트리밍 답변 확인.

#### Module 4: 상태 저장소 확장 (Persistence) ####
* 로컬 메모리의 한계(서버 재시작 시 기억 상실) 체감.
* DynamoDB Checkpointer 연결하여 멀티 인스턴스 환경에서도 대화 컨텍스트 유지하기.

#### Module 5: LangSmith #### 
* LangSmith를 연동하면 에이전트의 복잡한 추론 과정을 대시보드 

## 레퍼런스 ##
* https://docs.aws.amazon.com/ko_kr/prescriptive-guidance/latest/agentic-ai-frameworks/introduction.html

