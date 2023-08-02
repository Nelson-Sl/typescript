```mermaid
sequenceDiagram
	participant DNS Server
	participant Web Browser
	participant Web Server
	Web Browser->>Web Browser:解析URL
	Web Browser->>Web Browser:生成HTTP报文信息
	Web Browser->>DNS Server:查询IP地址
	DNS Server-->>Web Browser:IP地址
```

Knowledge List:
* [[02 DNS Server|DNS Server]]
* 