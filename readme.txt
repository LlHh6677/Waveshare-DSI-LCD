#第一步：下载并进入Waveshare-DSI-LCD驱动文件夹
git clone https://github.com/waveshare/Waveshare-DSI-LCD
cd Waveshare-DSI-LCD
 
#第二步：终端输入uname -a查看内核版本，并cd到对应文件目录
#5.15.61则运行下面指令
cd 5.15.61
 
#第三步：请确定当前使用的系统是多少位的，32位系统进入32目录，64位系统进入64目录
cd 32
#cd 64
 
#第四步：选择您对应的型号，复制指令安装驱动，如需修改I2C0 / I2C1，请注意选择正确的拨码开关再上电使用；
#2.8inch DSI LCD 480×640：
sudo bash ./WS_xinchDSI_MAIN.sh 28 I2C0

#4inch DSI LCD 480×800：
sudo bash ./WS_xinchDSI_MAIN.sh 40 I2C0

#7inch DSI LCD (C) 1024×600：
sudo bash ./WS_xinchDSI_MAIN.sh 70C I2C1

#7.9ich DSI LCD 400×1280：
sudo bash ./WS_xinchDSI_MAIN.sh 79 I2C0

#11.9inch DSI LCD 320×1480：
sudo bash ./WS_xinchDSI_MAIN.sh 119 I2C0

#8inch DSI LCD (C) 1280×800驱动：
sudo bash ./WS_xinchDSI_MAIN.sh 80C I2C0

#10.1inch DSI LCD (C) 1280×800驱动：
sudo bash ./WS_xinchDSI_MAIN.sh 101C I2C0
 
#第五步：等待几秒，当驱动安装完成，没有提示任何报错时，进行重启加载DSI驱动即可正常使用
sudo reboot

#注意：以上步骤需要确保树莓派可以正常连接到互联网。