### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>다른 예외 ObjectContext.CreateDatabase 및 DbProviderServices.CreateDatabase 메서드에 대 한 처리

|   |   |
|---|---|
|설명|.NET 4.5부터 데이터베이스 만들기에 실패하면 <code>CreateDatabase</code> 메서드는 빈 데이터베이스를 삭제하려고 합니다. 해당 작업에 성공하면 원래의 <xref:System.Data.SqlClient.SqlException?displayProperty=name>이 전파됩니다(항상 .NET 4.0에서 throw된 <xref:System.InvalidOperationException?displayProperty=name> 대신).|
|제안 해결 방법|Catch 하는 경우는 <xref:System.InvalidOperationException?displayProperty=name> 실행 하는 동안 <xref:System.Data.Objects.ObjectContext.CreateDatabase> 또는 <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions 이제도 발견 됩니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|
