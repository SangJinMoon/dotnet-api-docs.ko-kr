### <a name="deserialization-of-objects-across-appdomains-can-fail"></a>Appdomain 간 개체의 deserialization 실패할 수 있습니다.

|   |   |
|---|---|
|설명|경우에 따라, 응용 프로그램 기반이 다른 둘 이상의 앱 도메인이 앱에서 사용되는 경우 앱 도메인 간에 논리 호출 컨텍스트의 개체를 deserialize하려고 하면 예외가 throw됩니다.|
|제안 해결 방법|참조 [완화: 응용 프로그램 도메인 간 개체의 Deserialization](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)|
|범위|Microsoft Edge|
|버전|4.5.1|
|형식|런타임|

