### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>모든 자식 컨트롤에 영향을 TextBlock 컨트롤의 부모 IsEnabled 속성 변경

|   |   |
|---|---|
|설명|.NET Framework 4.6.2, 변경부터 <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> 의 부모는 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 컨트롤의 모든 자식 컨트롤 (예: 하이퍼링크 및 단추)에 영향을 줍니다는 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 제어 합니다. 내부.NET Framework 4.6.1에서 이전 버전을 제어는 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 항상의 상태를 반영 하지 않습니다는 <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> 의 속성은 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 부모 합니다.|
|제안 해결 방법|없음 이 변경은 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 컨트롤 내부에 있는 컨트롤의 정상적인 동작을 따릅니다.|
|범위|부|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|
