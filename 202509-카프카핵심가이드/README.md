
# 2025.08.20(수) Kafka 핵심 가이드 스터디 OT

## 인원
> ### `최윤진` - 커머스 기업 8년차 백엔드 개발자 <br>
> ### `신재익` - 이미지, 비전 AI 모델 개발 <br>
> ### `진현규` - 2년차 백엔드 개발자  <br>
> ### `일준` - 커머스 기업 2년차 백엔드 개발자 <br>
> ### `조범구` - 2년차 시스템 운영 및 개발 <br>
> ### `최민석` - 20년차 세일즈 엔지니어

### 스터디 일정
- 격주 수요일 저녁9시 진행 (2시간)
- 대략 1시간 발표 및 나머지 1시간은 내용 공유 및 토론 진행
- 스터디 진행은 3명이상 불참시 스터디 일정을 1주 미룬다, 단 격주로 진행하게 되는 만큼 전체일정이 1주 뒤가 아닌 해당 차수만 1주 미룬다.
- 차수별 발표자는 따로 정하지 않는다. 당일 사다리 타기로 발표자 지정 ( 일단 1명으로 진행, 진행 간 의견 반영하여 챕터별 1명씩으로 변경 가능 ).
    - 너무 바쁜나머지 준비를 못하거나, 안걸리겠지 하고 숨어있다가 발표자 당첨시 그다음 차수 발표 진행 .

- Youtube 녹화를 통한 증명 가능



### 스터디 진행 방식

- 진행하면서 일정은 자율적으로 변경 진행

##  1회차 - CH1 ~ 4 (P.80)
* 카프카 필요성 & 구조 이해
* 카프카 설치 및 실행
* 프로듀서/컨슈머 기본 메시지 송수신 실습
>
>
> * 카프카 필요성과 기존 메시징 시스템과 차이점
> * 브로커, 토픽, 파티션, 레플리카 개념
> * 로컬 설치 및 기본 실행
> * 프로듀서/컨슈머 기본 동작
>
> RabbitMq , ActiveMq  (Pub/Sub 모델 및 Queue 모델 비교) <br>
> Kafka Zookeeper -> KRaft 변경 사항 체크 ( version )
>

---

## 2회차 - CH 4 ~ 5 (P.55)
* 오프셋/리밸런스 관리, 독립 실행 컨슈머

> 오프셋 관리 및 커밋 전략 ( auto vs manual ) <br>
> 컨슈머 그룹과 리밸런싱 <br>
> 독립 실행 컨슈머  <br>
> AdminClient 토픽/설정/컨슈머 그룹 관리 <br>
>
> Kafka Consumer Group Rebalance 알고리즘 ( range, rr ) <br>
> Consumer Lag <br>
> AdminClient vs CLI <br>
> Schema Registry ( Confluent, AWS Glue )

---

## 3회차 - CH 6 ~ 7 (P.55)
* 클러스터, 복제, 요청 처리 구조 이해

> Cluster Membership Controller 역할 <br>
> 리더 / 팔로워 복제 구조 <br>
> 신뢰성 보장 수준 ack, min.insync.replicas <br>
>
> Kafka Controller Failover 과정
> ISR ( In-Sync Replica) 개념
> CAP 이론 Kafka (일관성 vs 가용성)
> 카프카 저장 방식 (로그 세그먼트, 페이지 캐시 등등)
> 고가용성(HA) 설계 고려사항
>

---

## 4회차 - CH 8 ~ 9 (P.55)
* 멱등적 프로듀서, 트랜잭션 이해

> 멱등성 프로듀서 <br>
> 트랜잭션 기반 메세지 처리 방식 <br>
> EOS (Exactly Once Sematics) <br>
> Kafka Connect 구조 장단점 <br>
> 트랜잭션 성능 오버헤드 실무 적용 사례
> Kafka Connect vs Flume, Logstash
> Schema Evolution
>

---

## 5회차 - CH10 ~ 11 (P.55)
* 멀티 클러스터 아키텍처, MirrorMaker 이해

> MirrorMaker2 개념, 아키텍처
> 멀티클러스터 설계 패턴 ( Active-Active, Active-Passive)
> 카프카 보안 (SSL, SASL)
>
> 보안 프로토콜 및 적용 시 성능 영향도

---

## 6회차 - CH11 ~ 12 (P.55)
* 인증/인가, 플랫폼 보안

> 주키퍼 or KRaft 보안
> 운영중인 카프카의 동적 설정 변경 및 파티션 관리
> Kafka ACL 관리
> Kafka on AWS MSK, Confluent Cloud 보안 차이점
> 파티션 Rebalance 데이터 이동 비용(?)

---

## 7회차 - CH13 ~ 14, Appendix (P.80)
* 카프카 모니터링 지표, Kafka Streams 활용 사례

> 카프카 모니터링 주요 지표  <br>
> Kafka Streams API 활용 <br>
> Prometheus + Grafana 를 활용하여 모니터링 가능한가.
> Stream-Table Duality 개념


---