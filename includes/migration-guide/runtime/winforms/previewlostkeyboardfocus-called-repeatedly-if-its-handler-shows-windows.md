### <a name="previewlostkeyboardfocus-is-called-repeatedly-if-its-handler-shows-a-windows-forms-message-box"></a>Windows Forms 메시지 상자를 표시 하는 처리기 경우 PreviewLostKeyboardFocus가 반복적으로 호출

|   |   |
|---|---|
|설명|.NET Framework 4.5부터 <xref:System.Windows.UIElement.PreviewLostKeyboardFocus> 처리기에서 <code>System.Windows.Forms.MessageBox.Show</code>를 호출하면 메시지 상자가 닫힐 때 처리기가 다시 발생하여 잠재적으로 메시지 상자의 무한 루프를 발생시킵니다.|
|제안 해결 방법|이 문제는 다음 두 가지 옵션으로 해결할 수 있습니다.<ol><li>이것은 <code>System.Windows.Forms.MessageBox.Show</code> 대신 <code>System.Windows.MessageBox.Show</code>를 호출하여 방지할 수 있습니다.</li><li>이것은 <xref:System.Windows.UIElement.LostKeyboardFocus> 이벤트 처리기에서 메시지 박스를 표시하여 방지할 수 있습니다(<xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=name> 이벤트 처리기와 반대).</li></ol>|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.ContentElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.IInputElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement3D.PreviewLostKeyboardFocus?displayProperty=nameWithType></li></ul>|

