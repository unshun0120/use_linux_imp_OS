# 1.install packages
step :    
1.打開終端機   
2.輸入 sudo  
3.輸入指令 sudo apt-get install build-essential nasm genisoimage bochs bochs-sdl 來安裝所需packages  

# 2.create loader.s file
step :    
1.打開終端機     
2.輸入 cd /home/unshun (切到要放loader.s該檔案的位置)    
3.輸入 touch loader.s (create file called "loader.s")  
4.輸入 chmod 777 loader.s (更改檔案權限之後可寫code進去)  
4.將程式寫入loader.s (程式在helloword資料夾底下,該程式目的是把數字0xCAFEBABE寫入eax暫存器內)  
5.到終端機輸入 nasm -f elf32 loader.s (把loader.s編譯成 32bits ELF object檔)，編譯完後就會看到同loader.s資料夾下有另外一個較loader.o的檔案  
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/10cc8ca1-717d-415c-84dd-07103bd34cec)
