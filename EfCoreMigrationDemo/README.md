# LFC.NET.Demo.Project
dotnet ef migrations add InitFristDB-2 --context BookStoreDbContext
dotnet ef database update --context BookStoreDbContext
dotnet ef migrations list --context BookStoreDbContext

dotnet ef migrations add InitSecondDB --context BookStoreSecondDbContext
dotnet ef database update --context BookStoreSecondDbContext
--创建用于 20220804115019_InitSecondDB 迁移的脚本
dotnet ef migrations script 0 20220804115019_InitSecondDB --context BookStoreSecondDbContext --output ./DB/InitSecondDB.sql


Add-Migration -Name InitFristDB -Context BookStoreDbContext
Update-Database -Context BookStoreDbContext
Get-Migration -Context BookStoreDbContext

Add-Migration -Name InitSecondDB -Context BookStoreSecondDbContext
Update-Database -Context BookStoreSecondDbContext
Get-Migration -Context BookStoreSecondDbContext