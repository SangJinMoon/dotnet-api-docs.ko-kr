### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 기본값은 이제 SHA256입니다.

|   |   |
|---|---|
|설명|.NET Framework 4.7.1부터 Msmq 메시지에 대한 WCF의 기본 메시지 서명 알고리즘은 SHA256입니다. .NET Framework 4.7 및 이전 버전에서 기본 메시지 서명 알고리즘은 SHA1입니다.|
|제안 해결 방법|.NET Framework 4.7.1 이상에서 이러한 변경 내용과의 호환성 문제가 발생하면 app.config 파일의 <code>&lt;runtime&gt;</code> 섹션에 다음 줄을 추가하여 변경 내용을 옵트아웃할 수 있습니다.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|런타임|

