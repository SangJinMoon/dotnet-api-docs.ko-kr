### <a name="serialport-background-thread-exceptions"></a>SerialPort 백그라운드 스레드 예외

|   |   |
|---|---|
|설명|<xref:System.IO.Ports.SerialPort> 스트림으로 생성된 백그라운드 스레드는 OS 예외가 발생할 때 더 이상 프로세스를 종료하지 않습니다. .NET Framework 4.7 이전 버전을 대상으로 하는 응용 프로그램에서는 <xref:System.IO.Ports.SerialPort> 스트림으로 생성된 백그라운드 스레드에서 운영 체제 예외가 throw될 때 프로세스가 종료됩니다. .NET Framework 4.7.1 이상 버전을 대상으로 하는 응용 프로그램에서는 백그라운드 스레드가 활성 직렬 포트와 관련된 OS 이벤트를 기다리고 갑자기 직렬 포트를 제거하는 등의 경우 충돌이 발생할 수 있습니다.|
|제안 해결 방법|.NET Framework 4.7.1을 대상으로 하는 앱의 경우, 필요하지 않으면 <code>app.config</code> 파일의 <code>&lt;runtime&gt;</code> 섹션에 다음을 추가하여 예외 처리를 옵트아웃할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>이전 버전의 .NET Framework를 대상으로 하지만 .NET Framework 4.7.1 이상에서 실행되는 앱의 경우 <code>app.config</code> 파일의 <code>&lt;runtime&gt;</code> 섹션에 다음 줄을 추가하여 예외 처리를 옵트인할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

