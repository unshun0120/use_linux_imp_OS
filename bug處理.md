# 1.無法開啟終端機(can not open terminal)
解決方法 : 
          1. 按下 Ctrl+Alt+(F1~F6)，按下其中一個會進入終端
          2. 輸入 sudo localectl set-locale LANG=en_US.UTF-8
          3. 若輸入2.的指令出現"...not in sudoers file..."，輸入 su (因為目前使用者沒有權限)，再輸入2.指令即
          4. 到/etc/default/locale檢查是否有更改到locale，有的話表示成功(不能直接到locale改是因為locale是read only)
          5. 之後關機重新啟動電源，即可開啟終端機
          (此過程主要是去更改lcoale裡的LANGUAGE改成en-US.UTF-8)
