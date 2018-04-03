# VisualStudio 2017

## 擴充套件

1. CodeMaid - 程式碼格式化
2. Bundler & Minifier - JavaScript, CSS 整合和壓縮
3. WebCompiler - 轉換 SCSS, LESS 成 CSS
4. Vue.js Pack - Vue.js Intellisense


## 建立 Entity Framework Core

僅提供在 NuGet 套件管理主控台下指令安裝, 無工具使用, 推測可能是為了配合 VS Code

### 1. 安裝套件
    PM> Install-Package Microsoft.EntityFrameworkCore.SqlServer
    PM> Install-Package Microsoft.EntityFrameworkCore.SqlServer.Design
    PM> Install-Package Microsoft.EntityFrameworkCore.Tools

### 2. 建立程式碼
    PM> Scaffold-DbContext "Server=.\SQLEXPRESS;Database=DbName;Persist Security Info=True;User ID=sa;Password=123"   Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -Force
* Scaffold-DbContext Tools 套件的指令，連線字串依自己情況決定
* -OutputDir 指定要輸出到專案根目錄下哪個資料夾
* -Force 工具產出的檔案強制覆寫現有的檔案，用於 Schema 異動後
* -Tables 指定資料表 e.g. Users, Roles
* -Verbose 將整個指令的執行過程顯示在管理主控台上
