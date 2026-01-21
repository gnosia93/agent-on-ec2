### 워크샵 아키텍처 ###
* 두뇌 (App): LangGraph (멀티 에이전트 및 루프 로직)
* 입구 (Serving): LangServe (FastAPI) (REST API 및 Playground 제공)
* 그릇 (Infra): Amazon EC2 + Golden Image (Packer) + Warm Pools
* 기억 (Persistence): Amazon DynamoDB (인스턴스가 교체되어도 대화 유지)
* 추론 (LLM): Amazon Bedrock (IAM Role을 통한 보안 연결
