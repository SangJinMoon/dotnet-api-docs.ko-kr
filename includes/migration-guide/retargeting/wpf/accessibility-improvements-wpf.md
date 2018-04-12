### <a name="accessibility-improvements-in-wpf"></a>WPF의 내게 필요한 옵션 기능 향상

|   |   |
|---|---|
|설명|<strong>높은 대비 개선 사항</strong><ul><li>에 대 한 포커스는 <xref:System.Windows.Controls.Expander> 컨트롤에 표시 됩니다. .NET Framework의 이전 버전에서는 없었습니다.</li><li>에 있는 텍스트 <xref:System.Windows.Controls.CheckBox> 및 <xref:System.Windows.Controls.RadioButton> 컨트롤 선택 하면 이전.NET Framework 버전에서 보다 보기 쉽게 되었습니다.</li><li>비활성화 된 테두리 <xref:System.Windows.Controls.ComboBox> 는 이제 사용할 수 없는 텍스트 색입니다. .NET Framework의 이전 버전에서는 없었습니다.</li><li>사용 안 함 및 포커스가 있는 단추는 이제 올바른 테마 색을 사용합니다. .NET Framework의 이전 버전에서는 구매 하지 않았는데 합니다.</li><li>드롭다운 단추 이제 경우에 표시 됩니다는 <xref:System.Windows.Controls.ComboBox> 컨트롤의 스타일으로 설정 되어 <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey?displayProperty=nameWithType>,.NET Framework의 이전 버전에서는 없었습니다.</li><li>정렬 표시기 화살표는 <xref:System.Windows.Controls.DataGrid> 컨트롤은 이제 테마 색을 사용 합니다. .NET Framework의 이전 버전에서는 제공 되지 않았습니다.</li><li>이제 기본 하이퍼링크 스타일 마우스를 위에 올바른 테마 색을 변경합니다. .NET Framework의 이전 버전에서는 제공 되지 않았습니다.</li><li>라디오 단추에 키보드 포커스 표시 됩니다. .NET Framework의 이전 버전에서는 없었습니다.</li><li><xref:System.Windows.Controls.DataGrid> 이제 확인란 열 컨트롤의 키보드 포커스 피드백에 대 한 예상 되는 색을 사용 합니다. .NET Framework의 이전 버전에서는 제공 되지 않았습니다.</li><li>키보드 포커스가 시각적 개체에 표시 됩니다. <xref:System.Windows.Controls.ComboBox> 및 <xref:System.Windows.Controls.ListBox>합니다. .NET Framework의 이전 버전에서는 없었습니다.</li></ul><strong>화면 판독기 상호 작용 기능 향상</strong><ul><li><xref:System.Windows.Controls.Expander> 컨트롤은 이제 올바르게 발표 그룹 (확장/축소)으로 화면 판독기입니다.</li><li><xref:System.Windows.Controls.DataGridCell> 이제 컨트롤 (지역화 된) 화면 판독기가 데이터 표 형태 셀으로 올바르게 발표 됩니다.</li><li>화면 판독기의 편집 가능한 이름을 공지 이제 <xref:System.Windows.Controls.ComboBox>합니다.</li><li><xref:System.Windows.Controls.PasswordBox> 컨트롤에 더 이상으로 알려집니다 &quot;보기에서 항목이&quot; 화면 판독기가 없습니다.</li></ul><strong>LiveRegion 지원</strong>내레이터 같이 화면 판독기 몰라도 UI 응용 프로그램의 일반적으로 사용자에 게 가장 적합 한 요소 것 이기 때문에 현재 포커스가 있는 UI에 대 한 항목을 기반으로 하는 데 도움이 됩니다. 그러나 UI 요소 화면에서 어딘가에 변경 하는 경우 포커스가 없는 사용자 수 하지 표시 하 고 중요 한 정보를 누락. 이 문제를 해결 하기 위해 LiveRegions 되어야 합니다. 개발자는 화면 판독기 또는 기타 [UI 자동화] 알리기 위해 사용할 수[UI 자동화 개요](~/docs/framework/ui-automation/ui-automation-overview.md) UI 요소에 중요 한 변경 사항에 대 한 클라이언트입니다. 화면 판독기는 사용자에게 이 변경 내용을 알리는 방법 및 시점을 결정할 수 있습니다. 또한 LiveSetting 속성에는 UI에 대 한 변경 내용을 사용자에 게에 얼마나 중요 한지 알고 화면 판독기를 수 있습니다.|
|제안 해결 방법|<strong>내부 / 외부로 이러한 변경 내용을 취소 하는 방법</strong>4.7.1.NET Framework에서 실행 해야 이러한 변경 내용에서 사용 하기 위해 응용 프로그램에 대 한 순서로 이상. 다음 방법 중 하나로 이러한 변경으로 인해 응용 프로그램을 활용할 수 있습니다.<ul><li>4.7.1.NET Framework를 대상으로 하는 것이 컴파일됩니다. 이러한 내게 필요한 옵션 변경은 4.7.1.NET Framework를 대상으로 하는 WPF 응용 프로그램에는 기본적으로 활성화 되어 이상입니다.</li><li>다음을 추가 하 여 레거시 내게 필요한 옵션 동작 부족 opts가 [AppContext 스위치](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) 에 <code>&lt;runtime&gt;</code> 다음 예제와 같이 false로 설정 하 고 응용 프로그램 구성 파일의 섹션입니다.</li></ul><pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>4.7.1.NET Framework를 대상으로 하는 응용 프로그램 이상 레거시를 보존 하려면 및 내게 필요한 옵션 동작을이 AppContext 스위치를 명시적으로 설정 하 여 사용 하는 레거시 내게 필요한 옵션 기능에 선택할 수 <code>true</code>합니다. UI 자동화의 개요를 참조 하십시오.는 [UI 자동화 개요](~/docs/framework/ui-automation/ui-automation-overview.md)합니다.|
|범위|주요함|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Automation.AutomationElementIdentifiers.LiveSettingProperty?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationElementIdentifiers.LiveRegionChangedEvent?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationLiveSetting?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.LiveSettingProperty?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.SetLiveSetting(System.Windows.DependencyObject,System.Windows.Automation.AutomationLiveSetting)?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.AutomationProperties.GetLiveSetting(System.Windows.DependencyObject)?displayProperty=nameWithType></li><li><xref:System.Windows.Automation.Peers.AutomationPeer.GetLiveSettingCore?displayProperty=nameWithType></li></ul>|
