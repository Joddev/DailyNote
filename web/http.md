### HTTP1.1 vs HTTP2.0

http 성능을 대폭 개선

- Multiplexed Streams(한 커넥션에 여러개의 메세지를 동시에 주고 받을 수 있음)
- Stream Prioritization(요청 리소스간 의존관계를 설정)
- Server Push(HTML문서상에 필요한 리소스를 클라이언트 요청없이 보내줄 수 있음)
- Header Compression(Header 정보를 HPACK압충방식을 이용하여 압축전송)

##### Reference

- [HTTP1.1 vs HTTP2.0 차이점 간단히 살펴보기](https://medium.com/@shlee1353/http1-1-vs-http2-0-%EC%B0%A8%EC%9D%B4%EC%A0%90-%EA%B0%84%EB%8B%A8%ED%9E%88-%EC%82%B4%ED%8E%B4%EB%B3%B4%EA%B8%B0-5727b7499b78)

