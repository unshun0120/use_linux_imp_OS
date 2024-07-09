# 1.取得stage2_eltorito file
參考medium上或是原文網站的github點進去會是404 not found，將網址中的github.com改成github.io即可成功下載檔案  
打開linux上的Firefox Web Browser，輸入以下網址並download下來，並放到 /home/unshun (放在跟kernel.elf檔案同一個位置)  
https://littleosbook.github.io/files/stage2_eltorito  

# 2.製作ISO image 
建資料夾來放kernel.elf和stage2_eltorito  
step :  
1.打開終端機，輸入 su  
2.輸入 mkdir -p iso/boot/grub (建立資料夾)  
&nbsp; &nbsp; 輸入 cp stage2_eltorito iso/boot/grub/ (把stage2_eltorito file放到iso/boot/grub底下)  
&nbsp; &nbsp; cp kernel.elf iso/boot/ (kernel.elf file放到iso/boot底下)  


