# docker-compose 폴더

## elk 폴더

Elasticsearch와 Kibana의 Apache 2.0 라이선스 소스 코드를 Elastic License와 SSPL(Server Side Public License)에 따라 이중 라이선스로 전환하여 사용자가 어느 라이선스를 적용할 지 선택할 수 있도록 변경되었다. (https://www.elastic.co/kr/pricing/faq/licensing 참조) 따라서, Apache 2.0 라이선스로 유지되는 elk stack 버전 7.10.2 이전 버전까지 사용하던지, Elasticsearch 7.10.2에서 파생한 Amazon의 OpenSearch의 사용을 권장한다.

## msa-template 폴더

MSA 템플릿을 위한 mesh, backend microservices 그리고 frontend 를 도커 컨테이너로 올릴 수 있도록 구성된 docker-compose 파일이다.
## mysql 폴더

mysql에 msaportal 와 예약(reservation) db를 생성한다.
## opensearch 폴더

아마존에서 Elasticsearch 7.10.2에서 파생한 Apache 2.0 라이선스의 OpenSearch로 centralized logging 관리 및 검색 기능을 제공한다.

## rabbitmq 폴더


## zipkin 폴더

Centralized Tracing 