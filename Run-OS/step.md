# 1.取得stage2_eltorito file
參考medium上或是原文網站的github點進去會是404 not found，將網址中的github.com改成github.io即可成功下載檔案  
打開linux上的Firefox Web Browser，輸入以下網址並download下來，並放到 /home/unshun (放在跟kernel.elf檔案同一個位置)  
https://littleosbook.github.io/files/stage2_eltorito  

# 2.製作ISO image 
step :  
1. 打開終端機，輸入 su  
2. 輸入 mkdir -p iso/boot/grub (建立資料夾) -> 輸入 cp stage2_eltorito iso/boot/grub/ (把stage2_eltorito file放到iso/boot/grub底下) -> 輸入cp kernel.elf iso/boot/ (kernel.elf file放到iso/boot底下)  
3. 輸入 cd /home/unshun/iso/boot/grub/ (cd到stage2_eltorito所在資料夾)-> 輸入 touch menu.lst -> 將程式寫入menu.lst內 (此file目的在於告訴GRUB會用到kernel的位置與一些資料)  
4. 輸入 cd /home/unshun (cd到iso資料夾的上一層，不是cd到iso此層) -> 輸入 genisoimage -R -b boot/grub/stage2_eltorito -no-emul-boot -boot-load-size 4 -A os -input-charset utf8 -quiet -boot-info-table -o os.iso iso (該指令用來生成 ISO Image)  
輸入完後會產生下圖該檔案  
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/1c0fb7c7-0e70-4975-874c-093841b43781)  

# 3.Run OS
step :  
1.輸入 touch bochsrc.txt -> chmod 777 bochsrc.txt -> 將程式許入bochsrc.txt內 (該程式用來設定一些config讓bochs可以運作)    
2.輸入 bochs -f bochsrc.txt -q 會跑出下圖視窗    
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/2a4f73ad-4339-4c1a-8a2a-8f329a56f458)  
3.跑出視窗後回到終端機輸入c，bochs才會運作把OS載入，按下後如下圖    
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/4dbce631-587b-4b20-934f-aca18cca928c)  
4.之後即可關掉bochs(即上圖視窗)，到終端機輸入 cat bochslog.txt (來顯示bochs的log)    
5.輸入後終端機會跑出很多東西，從裡面找到經由模擬器的CPU registers產生的RAX=00000000CAFEBABE或EAX=CAFEBABE值，代表成功，如下圖    
![image](https://github.com/unshun0120/use_linux_imp_OS/assets/79517348/e9878488-6333-439d-b50b-587c1e02fbb8)  




