# 🐧 Java/Fullstack 開發者：Linux 指令生存清單 (Dev Container 適用)

這份清單旨在幫助習慣 Windows 的開發者快速銜接 **Dev Container** 與 **WSL 2** 的 Linux 環境。

---

## 📂 1. 檔案與目錄操作 (File Management)
>
> **注意：** Linux 區分路徑的大小寫 (`Index.jsx` 與 `index.jsx` 是不同的)。

| 功能 | Linux 指令 | 說明 |
| :--- | :--- | :--- |
| **列出檔案** | `ls -al` | `a` 顯示隱藏檔（如 `.env`），`l` 顯示詳細權限與大小 |
| **切換目錄** | `cd <路徑>` | `cd ~` 回家目錄；`cd ..` 回上一層；`cd -` 回上一個目錄 |
| **顯示目前路徑** | `pwd` | 顯示目前的絕對路徑 (Print Working Directory) |
| **建立資料夾** | `mkdir -p <名稱>` | `-p` 確保父目錄不存在時會自動建立（例如 `mkdir -p src/main/java`） |
| **刪除檔案/目錄** | `rm -rf <名稱>` | **慎用！** `r` 遞迴刪除目錄，`f` 強制執行不詢問 |
| **移動或改名** | `mv <舊檔名> <新檔名>` | 將檔案移動至新位置，或直接原地改名 |
| **複製檔案/目錄** | `cp -r <來源> <目的>` | `-r` 用於複製整個資料夾（例如備份 `node_modules`） |

---

## 🔍 2. 內容查看與搜尋 (Search & View)
>
> 處理 Spring Boot Log 或大型 React 專案時的救星。

| 功能 | Linux 指令 | 說明 |
| :--- | :--- | :--- |
| **查看全檔案** | `cat <檔案>` | 一次印出所有內容。適合小檔案如 `pom.xml` 或 `.env` |
| **分頁查看** | `less <檔案>` | 適合大檔案，可用上下鍵捲動，按 `q` 離開 |
| **即時監控 Log** | `tail -f <檔案>` | **開發必備！** 持續追蹤並顯示檔案最後幾行的新內容 |
| **關鍵字搜尋** | `grep -i "ERROR" <檔名>` | 在檔案中尋找字串，`-i` 忽略大小寫 |
| **搜尋檔案** | `find . -name "*.java"` | 從目前目錄 `.` 開始向下尋找所有 `.java` 結尾的檔案 |

---

## 🛠️ 3. 系統與權限 (System & Permissions)

| 功能 | Linux 指令 | 說明 |
| :--- | :--- | :--- |
| **提升權限** | `sudo <指令>` | 以管理員 (root) 身份執行指令 |
| **修改執行權限** | `chmod +x <檔案>` | 讓腳本變為可執行（例如 `chmod +x mvnw`） |
| **查看進程** | `top` 或 `htop` | 類似工作管理員，按 `q` 結束。查看哪個 Java 進程佔用 CPU |
| **檢查連接埠** | `netstat -tulpn` | 查看 8080 (Spring) 或 3000 (React) 是否被佔用 |
| **強制刪除進程** | `kill -9 <PID>` | 當 Spring Boot 卡死關不掉時，強制結束該編號的進程 |

---

## ☕ 4. Java & Spring Boot 工具
>
> 在容器內請捨棄 `.exe` 或 `.bat` 的思維。

* **執行 Maven Wrapper:** `./mvnw clean install` (不要用 `mvnw.cmd`)
* **確認 Java 版本與位置:** `java -version`  
    `which java` (確認目前使用的是容器內哪一個 JDK)
* **手動啟動 JAR:** `java -jar target/your-app.jar`

---

## ⚛️ 5. Node.js & React 工具

* **完全重裝套件 (暴力法):** `rm -rf node_modules package-lock.json && npm install`
* **查看 Node 版本:** `node -v`
* **執行 Scripts:** `npm run dev` 或 `yarn start`

---

## 💡 終端機常用快捷鍵 (Keyboard Shortcuts)

* **`Tab`**: 自動補完指令或路徑（最強大的習慣，請務必養成）。
* **`Ctrl + C`**: 強制停止目前正在執行的程式（如關閉 Dev Server）。
* **`Ctrl + R`**: 搜尋曾經輸入過的歷史指令。
* **`↑` / `↓`**: 切換上一個/下一個使用過的指令。
* **`clear`**: 清空目前的終端機螢幕。
