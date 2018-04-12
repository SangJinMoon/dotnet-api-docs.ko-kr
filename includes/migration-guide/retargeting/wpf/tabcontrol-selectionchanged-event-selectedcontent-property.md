### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>TabControl SelectionChanged 이벤트와 SelectedContent 속성

|   |   |
|---|---|
|설명|4.7.1,.NET Framework부터는 <xref:System.Windows.Controls.TabControl> 의 값을 업데이트 해당 <xref:System.Windows.Controls.TabControl.SelectedContent> 발생 하기 전에 속성에서 <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> 해당 선택 항목 변경 될 때 이벤트를 합니다. .NET Framework 4.7 및 이전 버전에서는 SelectedContent에 대 한 업데이트 이벤트 이후에 발생 합니다.|
|제안 해결 방법|4.7.1.NET Framework를 대상으로 하거나 나중에 않을 수 있습니다이 앱을 변경 하 고 다음을 추가 하 여 레거시 동작을 사용 하 여는 <code>&lt;runtime&gt;</code> 응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>.NET Framework 4.7 또는 이전 이지만 대상으로 하는 응용 프로그램 4.7.1.NET Framework에서 실행 되 고 또는 나중에 다음 줄을 추가 하 여 새 동작을 활성화할 수는 <code>&lt;runtime&gt;</code> .configuration 응용 프로그램 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|
