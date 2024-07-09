# 1.create link.ld file
step :  
1. 打開終端機，輸入 su  
2. 輸入 cd /home/unshun  
3. 輸入 touch link.ld  
4. 輸入 chmod 777 link.ld  
5. 將程式寫入link.ld (該程式目的在於連接到linker讓loader.s成為一個可執行檔)  

# 2.將link.ld和loader.o連接起來
step :  
1. 打開終端機，輸入 su  
2. 輸入 ld -T link.ld -melf_i386 loader.o -o kernel.elf (將link.ld與loader.o連結，並產生一個可執行檔 called "kernel.elf")  
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/636c17db-d448-4f25-8d78-8ae9a40933ed)  

