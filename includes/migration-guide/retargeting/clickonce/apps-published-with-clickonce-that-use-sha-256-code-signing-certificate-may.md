### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Sha-256 코드 서명 인증서를 사용 하는 ClickOnce로 게시 된 앱 Windows 2003에서 실행 되지 않음

|   |   |
|---|---|
|설명|실행 파일이 SHA256으로 서명됩니다. 이전에는 코드 서명 인증서가 SHA-1 또는 SHA-256인지에 관계없이 SHA1로 서명되었습니다. 적용 대상:<ul><li>Visual Studio 2012 이상으로 빌드된 모든 응용 프로그램</li><li>.NET Framework 4.5가 있는 시스템에서 Visual Studio 2010 또는 이전 버전으로 빌드된 응용 프로그램</li></ul>또한 .NET Framework 4.5 이상이 있는 경우 컴파일 시의 대상 .NET Framework 버전에 관계없이 ClickOnce 매니페스트도 SHA-256 인증서에 대해 SHA-256으로 서명됩니다.|
|제안 해결 방법|ClickOnce 실행 파일을 서명 하는 변경 내용에는 Windows Server 2003 시스템을;만 영향을 줍니다. KB 938397을 설치 하는 것 필요로 합니다. .NET Framework 4.0 또는 이전 버전 응용 프로그램을 대상으로 하는 경우에 s h A-256으로 매니페스트에 서명 변경.NET Framework 4.5 이상 버전에서 런타임 종속성이 발생 합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|대상 변경|

