# VisualStudio 2017

## 擴充套件

1. CodeMaid - 程式碼格式化
2. Bundler & Minifier - JavaScript, CSS 整合和壓縮
3. WebCompiler - 轉換 SCSS, LESS 成 CSS
4. Vue.js Pack - Vuew.js Intellisense


## 建立 Entity Framework Core

因為 Entity Framework Core 可在 VS Code 上使用,
所以僅能用套件管理主控台下指令

### 1. 安裝套件
    PM> Install-Package Microsoft.EntityFrameworkCore.Tools
    PM> Install-Package Microsoft.EntityFrameworkCore.SqlServer.Design

### 2. 建立程式碼
    PM> Scaffold-DbContext "Server=.\SQLEXPRESS;Database=DbName;Persist Security Info=True;User ID=sa;Password=123"   Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -Force

    Scaffold-DbContext為剛剛安裝Tools套件的指令，連線字串依自己情況決定
    -OutputDir指定要輸出到專案根目錄下哪個資料夾，本文為Models資料夾
    -Force為工具產出的Class檔案強制覆寫現有的檔案(DB欄位Schema異動後，就給這個)
