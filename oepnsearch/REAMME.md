# OpenSearch

- https://opensearch.org/docs/latest/
- https://opensearch.org/downloads.html
- https://github.com/opensearch-project/OpenSearch
- https://github.com/opensearch-project/OpenSearch-Dashboards
- https://opensearch.org/docs/latest/clients/logstash/index/

## docker-compose.yml

elasticsearch 를 대체하는 opensearch, kibana 를 대체하는 opensearch-dashboards 그리고, logstash-oss-with-opensearch-output-plugin 의 도커 파일들을 하나로 묶어준다.

- OpenSearch: Data store and search engine
- OpenSearch Dashboards: Search frontend and visualizations
- logstash-oss-with-opensearch-output-plugin: real-time event processing engine

## OpenSearch 확인

브라우저에서 다음 URL로 이동하여 admin / admin 으로 접속한다.

```
http://localhost:5601/
```

## Logstash 확인

logstash 폴더의 config/logstash.yml 과 pipeline/logstash.conf 환경설정으로 구동된다.
logstash의 pipeline은 input, filter, output으로 구성된다.

- input: 마이크로서비스들로부터 log 이벤트들을 받는다
- filter: input으로 받은 이벤트들을 output으로 전송하기 전에 원하는 형태로 변형한다.
- output: OpenSearch 로 filtered 이벤트들을 전송한다.

최종 30 라인을 실시간 로그를 확인할 수 있다.

```
docker logs --tail 30 -f logstash
```
