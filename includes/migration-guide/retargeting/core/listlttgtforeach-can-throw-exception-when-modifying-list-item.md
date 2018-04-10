### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a>목록&lt;T&gt;합니다. 목록 항목을 수정 하는 경우 ForEach 예외를 throw 할 수 있습니다.

|   |   |
|---|---|
|설명|.NET 4.5부터는 <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> 열거자를 throw 합니다는 <xref:System.InvalidOperationException?displayProperty=name> 호출 컬렉션의 요소가 수정 된 경우는 예외입니다. 이전에는 예외를 throw하지 않고 경합 상태가 발생할 수 있었습니다.|
|제안 해결 방법|이상적으로, 안전한 작업을 위해 요소를 열거하는 동안 목록을 수정하지 않도록 코드를 수정해야 합니다. 그러나 이전 동작으로 되돌리려면 응용 프로그램이 .NET 4.0을 대상으로 할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|

