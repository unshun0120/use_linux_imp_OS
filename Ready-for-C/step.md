# 1.create kmain.c
create一個kmain function，之後會被loader.s使用  
step :  
1. 輸入 touch kmain.c -> chmod 777 kmain.c  
2. 將程式寫入kmain.c

# 2.create Makefile
step :    
1. 輸入 touch Makefile -> chmod 777 Makefile    
2. 將程式寫入Makefile  

# 3.編譯Makefile
1. 輸入 make run，編譯若通過則會開啟bochs

*** 若輸入"make run"後出現 "Makefile:10: *** missing separator.  Stop." 錯誤訊息  
   例 : ![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/dec0989a-eddb-483c-a832-8bc6b57c5709)  
   此錯誤訊息表示Makefile文件中第10行的空白部分要用tab不要用4空格取代  
   下圖是Makefile第10行空白部分用4個空格隔開  
   ![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/df15acf3-8fc4-417f-905d-8d61a8920c6f)  
   將4個空格刪除並用一個tab取代會如下圖 :  
   ![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/22717cd3-fcb8-4c1c-8526-ccfdc5918135)    
   其他空白部分以此類推則可以solve此bug ***
 
