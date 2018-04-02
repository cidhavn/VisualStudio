# VisualStudio 2017

擴充套件

1. CodeMaid - 程式碼格式化
2. Bundler & Minifier - JavaScript, CSS 整合和壓縮
3. WebCompiler - 轉換 SCSS, LESS 成 CSS
4. Vue.js Pack - Vuew.js Intellisense


Use Entity Framework Core

因為 Entity Framework Core 可在 VS Code 上使用,
所以僅能用套件管理主控台下指令

Step 1. 安裝套件
1.PM> Install-Package Microsoft.EntityFrameworkCore.Tools
2.PM> Install-Package Microsoft.EntityFrameworkCore.SqlServer.Design

Step 2. 建立程式碼
1.PM> Scaffold-DbContext "Server=.\SQLEXPRESS;Database=DbName;Persist Security Info=True;User ID=sa;Password=123" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -Force
