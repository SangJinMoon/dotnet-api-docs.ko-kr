### <a name="glyphruncomputeinkboundingbox-and-formattedtextextent-return-different-values-beginning-in-net-45"></a>.NET 4.5부터 GlyphRun.ComputeInkBoundingBox() 및 FormattedText.Extent가 다른 값을 반환합니다.

|   |   |
|---|---|
|설명|.NET Framework 4.0의 일부 경우에서 포함된 문자 모양에 대해 상자가 너무 작은 문제를 해결하기 위해 .NET Framework 4.5에서 <xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox> 및 <xref:System.Windows.Media.FormattedText.Extent>를 개선하였습니다. 결과적으로 .NET Framework 4.5부터 일부 경계 상자가 커져 UI 레이아웃에 미묘한 차이가 발생합니다.|
|제안 해결 방법|일부 문자 모양 경계 상자의 크기가 커졌습니다. 이러한 변경은 일반적으로 프레젠테이션 및 적중 상자 테스트를 향상시키지만 이전 동작(.NET 4.5 전)이 필요할 경우 app.config 파일에 다음의 항목을 추가하여 사용할 수 있습니다.<pre><code class="language-xml">&lt;appsettings&gt;&#13;&#10;&lt;add key=&quot;IncludeAllInkInBoundingBox&quot; value=&quot;false&quot;&gt;&#13;&#10;&lt;/appsettings&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox?displayProperty=nameWithType></li><li><xref:System.Windows.Media.FormattedText.Extent?displayProperty=nameWithType></li></ul>|

