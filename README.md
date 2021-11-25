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
<h3>命令列模式<h3>
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
   
     
