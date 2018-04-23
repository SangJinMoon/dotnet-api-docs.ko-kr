### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter는 해시 테이블과 순서가 지정된 유사 컬렉션 개체를 역직렬화할 수 없습니다

|   |   |
|---|---|
|설명|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name>은 하나의 .NET Framework 버전에서 직렬화된 개체가 다른 버전에서 성공적으로 역직렬화하는 것을 보장하지 않습니다. 특히, 일부 순서가 지정된 컬렉션(예: <xref:System.Collections.Hashtable?displayProperty=name>)은 4.0 및 4.5 간에 멤버가 추가되었으며 이러한 형식의 개체가 .NET 4.5로 직렬화된 경우 .NET 4.0으로 역직렬화할 수 없습니다. 직렬화된 데이터가 같은 .NET Framework 버전으로 직렬화 및 역직렬화되면 문제가 발생하지 않습니다.|
|제안 해결 방법|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> 직렬화는 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> 직렬화 또는 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>으로 대체되어야 .NET Framework 변경 시 복원이 가능합니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

