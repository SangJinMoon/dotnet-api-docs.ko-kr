### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>AntiXSSEncoder를 사용 하는 경우 여러 줄 TextBox ASP.Net 간격 변경

|   |   |
|---|---|
|설명|.NET Framework 4.0에서 <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>을 사용하는 경우 추가 줄은 포스트백에서 여러 줄 텍스트 상자의 줄 사이에 삽입되었습니다. .NET Framework 4.5에서는 웹 응용 프로그램이 .NET 4.5를 대상으로 하는 경우를 제외하고 이러한 추가 줄 바꿈이 포함되지 않습니다.|
|제안 해결 방법|.NET 4.5로 대상이 다시 지정된 4.0 웹 응용 프로그램에는 더 이상 추가 줄 바꿈을 삽입하지 않도록 개선된 여러 줄 텍스트 상자가 있을 수 있습니다. 필요 없는 경우에 응용 프로그램에서.NET Framework 4.0을 대상으로 하 여.NET Framework 4.5에서 실행 하는 경우 이전 동작에 있을 수 있습니다.|
|범위|부|
|버전|4.5|
|형식|대상 변경|

