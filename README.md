# CS_NOTE
<h3>linux背景知識<h3>
 <h5>
 是一個自由和開放原始碼的類Unix作業系統
 <br>
 <br>
 版本會分為"開發中版本範例"以及"穩定版本範例"
 <br>
 <br>
 並且有提供線上升級機制
 <h5>
<h3>檔案命名原則<h3>
 <h5>區分英文字元大小寫，通常以小寫為主
  <br>
  <br>
  檔案最多256字元，可包括字母、數字、點、下劃線、連字元
  <br>
  <br>
  不可包括問號、星號、空格、錢字號、擴號、斜線
 <h5>
<h3>
<h3>絕對路徑與相對路徑<h3>
 <h5>絕對路徑:一定由「根目錄/」寫起
  <br>
  <br>
     相對路徑:相對於目前工作目錄的路徑，寫成「cd../man」
 <h5>
<h3>基本指令<h3>
 <h5>- cd &nbsp 變換目錄
  <br>
  <br>
     - pwd &nbsp 顯示目前目錄
  <br>
  <br>
     - mkdir &nbsp 建立一個新的目錄
  <br>
  <br>
     - rmdir &nbsp 刪除一個空目錄
  <br>
  <br>
     - cp &nbsp 複製
  <br>
  <br>
     - mv &nbsp 移動
  <br>
  <br>
     - ls &nbsp 顯示目錄下所有內容
  <br>
  <br>
     - cat &nbsp 查看檔案內容
 <h5>
<h3>編輯文檔<h3>
 <h3>nano<h3>
  <h5>- ctrl c : 顯示游標所在
  <br>
  <br>
  - ctrl w : 查詢命令，按下後會跳回末行反白位置，輸入要查詢的內容即可
  <br>
  <br>
  - ctrl o : 寫入
  <br>
  <br>
  - ctrl x : 退出
  <h5>
 <h3>vi/vim<h3>
  <h5>一般模式:
   <br>
   <br>
   可是使用上下左右標移動、刪除字元以及複製貼上檔案
   <br>
   <br>編輯模式:
   <br>
   <br>
   編輯文字，i鍵進入編輯模式，ESC即退出編輯模式
  <h5>
**命令提示字元**   
  <h5>- : w  &nbsp 將編輯的資料寫入檔案中
  <br>
  <br>
  - : w ! &nbsp 若檔案屬性為「唯讀」時，強制寫入該檔案
  <br>
  <br>
  - : q &nbsp 離開
  <br>
  <br>
  - : q ! &nbsp 強制結束並離開
  <br>
  <br>
  - : wq &nbsp 儲存後離開 (若為 : wq ! 則為強制儲存後離開)
  <br>
  <br>
  - : w [ filename ] &nbsp 另存新檔
  <br>
  <br>
  - : r [ filename ] &nbsp 在編輯的資料中， 讀入另一個檔案的資料
  <br>
  <br>
  - : set nu &nbsp 顯示行號，設定後會在每一行的字首顯示該行行號
  <h5>
   
<h3>使用者與群組<h3>
   <h3>使用者分類<h3>
    <h5>
    - user
   <br>
   <br>
    - group
   <br>
   <br>
    - others<h5>
   <h3>群組(group)主要意義<h3>
    <h5>- 將帳號歸類，有助於專案開發
     <br>
     <br>
     -  每個使用者均可加入多個群組
     <h3>關於身份類別：<h3>
<h5>系統管理員： root
 <br>
 <br>
一般帳號：
 <br>
 <br>
 &nbsp - 系統帳號 (用於系統帳號的工作)
 <br>
 <br>
 &nbsp - 一般使用者帳號 (用於一般使用者登入用。)
<h5>
<h3>檔案系統目錄結構<h3>
 <h5> /.(根目錄)
  <br>
  <br>
  /bin：
bin 是 Binaries (二進位制檔案) 的縮寫, 這個目錄存放著最經常使用的命令。
  <br>
  <br>
/boot：
這裡存放的是啟動 Linux 時使用的一些核心檔案，包括一些連線檔案以及映象檔案。
<br>
  <br>
/dev ：
dev 是 Device(裝置) 的縮寫, 該目錄下存放的是 Linux 的外部裝置，在 Linux 中訪問裝置的方式和訪問檔案的方式是相同的。
<br>
<br>
/etc：
etc 是 Etcetera(等等) 的縮寫,這個目錄用來存放所有的系統管理所需要的配置檔案和子目錄。
<br>
  <br>
/home：
使用者的主目錄，在 Linux 中，每個使用者都有一個自己的目錄，一般該目錄名是以使用者的賬號命名的，如上圖中的 alice、bob 和 eve。
<br>
  <br>
/lib：
lib 是 Library(庫) 的縮寫這個目錄裡存放著系統最基本的動態連線共享庫，
  <br>
  <br>
  其作用類似於 Windows 裡的 DLL 檔案。幾乎所有的應用程式都需要用到這些共享庫。
<br>
  <br>
/lost+found：
這個目錄一般情況下是空的，當系統非法關機後，這裡就存放了一些檔案。
<br>
  <br>
/media：
linux 系統會自動識別一些裝置，例如U盤、光碟機等等，當識別後，Linux 會把識別的裝置掛載到這個目錄下。
<br>
  <br>
/mnt：
系統提供該目錄是為了讓使用者臨時掛載別的檔案系統的，我們可以將光碟機掛載在 /mnt/ 上，然後進入該目錄就可以檢視光碟機裡的內容了。
<br>
  <br>
/opt：
opt 是 optional(可選) 的縮寫，這是給主機額外安裝軟體所擺放的目錄。比如你安裝一個ORACLE資料庫則就可以放到這個目錄下。預設是空的。
<br>
  <br>
/proc：
proc 是 Processes(程序) 的縮寫，/proc 是一種偽檔案系統（也即虛擬檔案系統），
  <br>
  <br>
  儲存的是當前核心執行狀態的一系列特殊檔案，這個目錄是一個虛擬的目錄，它是系統記憶體的對映，我們可以通過直接訪問這個目錄來獲取系統資訊。
  <br>
  <br>
這個目錄的內容不在硬碟上而是在記憶體裡，我們也可以直接修改裡面的某些檔案，比如可以通過下面的命令來遮蔽主機的ping命令，
  <br>
  <br>
  使別人無法ping你的機器
  <br>
  <br>
/root：
該目錄為系統管理員，也稱作超級許可權者的使用者主目錄。
<br>
  <br>
/sbin：
s 就是 Super User 的意思，是 Superuser Binaries (超級使用者的二進位制檔案) 的縮寫，這裡存放的是系統管理員使用的系統管理程式。
<br>
  <br>
/selinux：
這個目錄是 Redhat/CentOS 所特有的目錄，Selinux 是一個安全機制，類似於 windows 的防火牆，
  <br>
  <br>
  但是這套機制比較複雜，這個目錄就是存放selinux相關的檔案的。
<br>
  <br>
/srv：
該目錄存放一些服務啟動之後需要提取的資料。
<br>
  <br>
/sys：
這是 Linux2.6 核心的一個很大的變化。該目錄下安裝了 2.6 核心中新出現的一個檔案系統 sysfs 。
<br>
  <br>
  sysfs 檔案系統集成了下面3種檔案系統的資訊：針對程序資訊的 proc 檔案系統、針對裝置的 devfs 檔案系統以及針對偽終端的 devpts 檔案系統。
  <br>
  <br>
該檔案系統是核心裝置樹的一個直觀反映。
  <br>
  <br>
當一個核心物件被建立的時候，對應的檔案和目錄也在核心物件子系統中被建立。
<br>
  <br>
/tmp：
tmp 是 temporary(臨時) 的縮寫這個目錄是用來存放一些臨時檔案的。
<br>
  <br>
/usr：
usr 是 unix shared resources(共享資源) 的縮寫，這是一個非常重要的目錄，使用者的很多應用程式和檔案都放在這個目錄下，類似於 windows 下的 program files 目錄。
<br>
  <br>
/usr/bin：
系統使用者使用的應用程式。
<br>
  <br>
/usr/sbin：
超級使用者使用的比較高階的管理程式和系統守護程式。
<br>
  <br>
/usr/src：
核心原始碼預設的放置目錄。
<br>
  <br>
/var：
var 是 variable(變數) 的縮寫，這個目錄中存放著在不斷擴充著的東西，我們習慣將那些經常被修改的目錄放在這個目錄下。包括各種日誌檔案。
<br>
  <br>
/run：
是一個臨時檔案系統，儲存系統啟動以來的資訊。當系統重啟時，這個目錄下的檔案應該被刪掉或清除。如果你的系統上有 /var/run 目錄，應該讓它指向 run。
 <h5>  
<h3>更改使用者權限<h3>
 <h5>- u：檔案擁有者
  <br>
  <br>
- g：與該檔案的擁有者同一個群體者
  <br>
  <br>
- o：其他以外的人
  <br>
  <br>
- a：三者皆是
  <br>
  <br>
- +：增加許可權
  <br>
  <br>
- -：取消許可權
  <br>
  <br>
- =：唯一設定許可權
  <br>
  <br>
- r：可讀取
  <br>
  <br>
- w：可寫入
  <br>
  <br>
- x：可執行
  <br>
  <br>
- chmod 可控制檔案如何被他人調用→ chmod [-cfvR] [--help] [--version] mode file…
   <br>
  <br>
- mode 許可權設定字串 → [ugoa...][[+-=][rwxX]...][,...]
   <br>
  <br>
- chown 可修改檔案或目錄擁有者及群組
   <br>
  <br>
- ls -l 可查看每個檔案與目錄的擁有者與群組
<h5>
 <h3>壓縮檔案<h3>
  <h5>
   為什麼要壓縮檔案呢？
    <br>
  <br>
1.備份資料的時候，方便整理。
    <br>
  <br>
2.將檔案變小，節省電腦硬碟的空間。(但圖片、音訊、視訊等多媒體檔案壓縮率低，並不能有效節省空間)
    <br>
  <br>
3.將無數個散亂的檔案打包成一個較小的檔案，亦方便資訊在網路上流通。(可將永久免費版之付費軟體輕鬆分享)
    <br>
  <br>
4.壓縮檔案時，可以視情況進行加密。
    <br>
  <br>
壓縮檔案的概念？
    <br>
  <br>
使用的電腦系統是使用bytes單位計量的，但事實上電腦最小的計量單位應該是 bits (1 byte = 8 bits)。
    <br>
  <br>
因此將許多閒置的空間釋出，即可將檔案占用的空間減少。
    <br>
  <br>
將重複的資料進行統計記錄。EXAMPLE：如果資料為『111....』共有100個1時，
    <br>
  <br>
那麼壓縮技術會記錄『100個1』而不是真的有100個1的位元存在。
<h5>
 <h3>各壓縮的差別<h3>
  <h5>
1.需要在記憶體很小的機器（如小於 128MB）上解壓縮時，則選擇 gzip 格式。
     <br>
  <br>
2.需要在很簡單、沒有什麼工具可用的機器解壓縮時，則選擇 gzip 格式。
     <br>
  <br>
3.需要節省網路頻寬、縮短下載所需要的時間時，則選擇 xz 格式。
     <br>
  <br>
4.需要有最好的壓縮率時，則選擇 tar.xz  格式。
     <br>
  <br>
5.需要在記憶體很小的機器（如小於 128MB）上解壓縮時，則選擇 gzip 格式。
   <br>
  <br>
6.需要在很簡單、沒有什麼工具可用的機器解壓縮時，則選擇 gzip 格式。
   <br>
  <br>
7.需要節省網路頻寬、縮短下載所需要的時間時，則選擇 xz 格式。
   <br>
  <br>
8.需要有最好的壓縮率時，則選擇 tar.xz  格式。
   <h3>壓縮檔案實作<h3>
 <h5>
* gzip
壓縮：gzip FileName
   <br>
  <br>
解壓縮：
   <br>
  <br>
gunzip FileName.gz
   <br>
  <br>
gzip -d FileName.gz
 <br>
  <br>
 * xz
  <br>
  <br>
壓縮：xz -z FileName
  <br>
  <br>
解壓縮：xz -d FileName.xz
  <br>
  <br>
* tar.gz
  <br>
  <br>
壓縮：tar -zcvf FileName.tar.gz DirName
  <br>
  <br>
解壓縮：tar -zxvf FileName.tar.gz
  <br>
  <br>
  <h3>檔案搜尋<h3>
   <h5>
    find [path] [option] [action] filename
* option
    <br>
  <br>
-size EX：找出大於500M的檔案→-size +500M
    <br>
  <br>
-name EX：找出為照片的檔案→-name "*.jpg"
    <br>
  <br>
-type EX：-type f→一般檔案;-type d→一般目錄
    <br>
  <br>
-user EX：同時找兩個擁有者的檔案→-user user1 -o -user user2
    <br>
  <br>
*action -exec
    <br>
  <br>
ls
    <br>
  <br>
print
* which filename
 <br>
  <br>
-n<文件名长度>指定文件名長度，指定的長度必須大於或等於所有文件中最長的文件名。
     <br>
  <br>
-p<文件名長度>與-n参數相同，但此處的<文件名長度>包括了文件的路徑。
     <br>
  <br>
-w指定輸出欄位的寬度。
     <br>
  <br>
-V顯示版本訊息。
    <br>
    <br>
    * cat  從第一行顯示檔案內容、形成新檔案
    <br>
    <br>
cat -n file1 > file2→把file1的檔案內容加上行號後輸入file2檔案
    <br>
    <br>
-n→由1開始對所有輸出的行數編號
    <br>
    <br>
>→將多個文件覆蓋到目標文件中
    <br>
    <br>
>>→將多個文件追加到目標文件中
    <br>
    <br>
* tac  從最後一行開始顯示
    <br>
    <br>
tac -r -s 'x\|[^x]' test.log→一個接著一個字符的反轉一個文件
    <br>
    <br>
-r→將分隔符作為基礎正規表達是處理
    <br>
    <br>
-s→使用String作為分隔符代替默認的換行符
    <br>
    <br>
   * more 一頁一頁的顯示檔案內容
     <br>
    <br>
more +20 testfile→從第20行開始顯示testfile的文檔內容
     <br>
    <br>
ENTER：向下n行(default為1行)
     <br>
    <br>
Ctrl+F/SPACE：向下滾動一屏
     <br>
    <br>
Ctrl+B：返回上一屏
     <br>
    <br>
less 與 more 類似，顯示檔案室允許用戶既可以向前又可以向後翻頁閱讀檔案
     <br>
    <br>
ps -ef |less→ps查看進程信息並通過less分頁顯示	
     <br>
    <br>
j→下一行
     <br>
    <br>
k→上一行
     <br>
    <br>
G→移動到最後一行
     <br>
    <br>
g→移動到第一行
     <br>
    <br>
   * head/tail 只看頭/尾巴幾行
  <br>
    <br>
    head -n 20 state.txt | tail -10→顯示11~20行的內容
    <h5>
     <h3>資料傳輸<h3>
      <h5>HTTP超文本傳輸協定(HyperText Transfer Protocol)
       <br>
    <br>
協定內容：
       <br>
    <br>
1. 標準化內容格式
       <br>
    <br>
2. 分為 header 跟 body
       <br>
    <br>
3. 用狀態碼標準化結果   （Http Status Code）
       <br>
    <br>
4. 用動詞標準化請求方法  （Http Request Method）
<h5>
 <h3>http request method<h3>
  <h5>- GET
     <br>
    <br>
GET 方法請求展示指定資源。使用 GET 的請求只應用於取得資料。
     <br>
    <br>
- HEAD (en-US)
     <br>
    <br>
HEAD 方法請求與 GET 方法相同的回應，但它沒有回應主體（response body）。
     <br>
    <br>
- POST
     <br>
    <br>
POST 方法用於提交指定資源的實體，通常會改變伺服器的狀態或副作用（side effect）。
     <br>
    <br>
- PUT (en-US)
     <br>
    <br>
PUT 方法會取代指定資源所酬載請求（request payload）的所有表現。
     <br>
    <br>
- DELETE (en-US)
     <br>
    <br>
DELETE 方法會刪除指定資源.
     <br>
    <br>
- CONNECT
     <br>
    <br>
CONNECT 方法會和指定資源標明的伺服器之間，建立隧道（tunnel）。
     <br>
    <br>
- OPTIONS (en-US)
     <br>
    <br>
OPTIONS 方法描述指定資源的溝通方法（communication option）。
     <br>
    <br>
- TRACE (en-US)
     <br>
    <br>
TRACE 方法會與指定資源標明的伺服器之間，執行迴路返回測試（loop-back test）。
     <br>
    <br>
- PATCH (en-US)
     <br>
    <br>
PATCH 方法套用指定資源的部份修改。

<h5>
 <h3>TCP/IP<h3>
  <h5>
   TCP/IP提供了點對點的連結機制，將資料應該如何封裝、定址、傳輸、路由以及在目的地如何接收，
    <br>
    <br>
   都加以標準化。它將軟體通信過程抽象化為四個抽象層，採取協議堆疊的方式，
    <br>
    <br>
   分別實作出不同通信協定。協定套組下的各種協議，
    <br>
    <br>
   依其功能不同，被分別歸屬到這四個階層之中，常被視為是簡化的七層OSI模型。
    <br>
    <br>
   當瀏覽器輸入網址，發出一個 GET 請求時
   <br>
    <br>
1.TCP三向交握:在瀏覽器送出請求之後，瀏覽器和伺服器就會開始初步溝通，
    <br>
    <br>
   確定雙方的溝通管道順暢，以便後續請求的執行
    <br>
    <br>
2.瀏覽器請求、資料傳輸、渲染畫面如同前面所提，當三項交握結束後，
    <br>
    <br>
   瀏覽器和伺服器便會開始執行請求、資料傳輸與渲染畫面的過程
    <br>
    <br>
3.TCP四次揮手，結束連線在網頁成功渲染之後，瀏覽器就會和伺服器進行最後的溝通，
    <br>
    <br>
   確認傳輸過程已完成，準備結束連線
   <h5>
<h3>網路相關<h3>
 <h5>
  * route
  <br>
    <br>
add : 新增一條路由規則
   <br>
    <br>
del : 刪除一條路由規則
   <br>
    <br>
-net : 目的地址是一個網路
   <br>
    <br>
-host : 目的地址是一個主機
   <br>
    <br>
target : 目的網路或主機
   <br>
    <br>
netmask : 目的地址的網路掩碼
   <br>
    <br>
gw : 路由資料包通過的閘道器
   <br>
    <br>
dev : 為路由指定的網路介面
  <br>
    <br>
* ping
  常用網路檢測工具，可藉由發送 ICMP ECHO_REQUEST 封包，
  <br>
    <br>
  檢查自己與特定設備之間的網路是否暢通，並同時測量網路連線的來回通訊延遲時間（round-trip delay time）。
  <br>
    <br>
-n：參數指定封包數→EX：ping -n 10 blog.gtwang.org
  <br>
    <br>
-t：持續監看網路是否正常→EX：ping -t blog.gtwang.org
  <br>
    <br>
-4/-6：IPv4/IPv6-c：指定Ping次數→EX：ping -c 4 blog.gtwang.org
  <br>
    <br>
-s：指定發送的數據字結數→EX：ping -s 1024 facebook.com
  <br>
    <br>
-i：指定收發資訊間隔時間→EX：ping -i 0.4 facebook.com
  <br>
    <br>
*影響網路速度的因素：
  <br>
    <br>
延遲（Latency）：封包從來源端至目的端中間所花的時間
  <br>
    <br>
頻寬（Bandwidth）：傳輸媒介的最大吞吐量
  <br>
    <br>
*網路延遲（Latency）的組成元素:
  <br>
    <br>
propagation delay：封包在網路線上傳輸所花費的時間，與網路線上電子訊號跑的速度有關，這個時間就是距離除以訊號傳送速度所得到的數值。
  <br>
    <br>
transmission delay：網路卡將資料傳送到網路線上所花的時間，與網路設備的傳送速度有關。
  <br>
    <br>
nodal processing delay：路由器處理封包表頭、檢查位元資料錯誤與尋找配送路徑等所花費的時間。
  <br>
    <br>
queuing delay：路由器因為某些因素無法立刻將封包傳送到網路上，造成封包暫存在佇列中等待的時間。
  <br>
    <br>
  *netstart
  <br>
    <br>
  查看端口是否被占用：netstat -a|grep 3306
  <br>
    <br>
查看數據包統計信息：netstat -s
  <br>
    <br>
查看路由信息：netstat -r




