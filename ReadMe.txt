ESP32S3 Lilygo t-displayS3 Touch

Upload using Espressif Flash Tool
0x0 touchSlider100.ino.bootloader.bin
0x8000 touchSlider100.ino.partitions.bin
0xe000 boot_app0.bin
0x10000 touchSlider100.ino.bin

After ESP32 boot wait for 3 min until network scanning is completed.
Open the wifi in your phone and search for AH_Radio
Connect to your network
Wait for 5 min for the Spiff format to be completed
Look at the LCD for the IP address
connect to that Ip Address using your computer browser
upload single station or list of stations using the following format

Station Name 1,Station Address 1
Station Name 2,Station Address 2

Radio Ariel,http://123.456.789.0/stream
Radio Hits,http://stream.awesomehitsradio.com
.
.
.
You can find station URL's here: https://streamurl.link/ 
.
Connect the I2S DAC to the following pins:
#define I2S_BCLK 12
#define I2S_LRC 11
#define I2S_DOUT 13

Note: 1. The boot_app0.bin file is included with the Lilygo flash tool in the bin directory.
       2. An I2S DAC is required for this project, Amplifier is optional.  Consult the I2S data sheet to learn how to activate the (L+R)/2 or stereo signal.  
Note: for some stations that doesn't play and starts with https:// try to change to http:// and check if it is working

/*ESP32S3*/
#define PIN_LCD_BL 38

#define PIN_LCD_D0 39
#define PIN_LCD_D1 40
#define PIN_LCD_D2 41
#define PIN_LCD_D3 42
#define PIN_LCD_D4 45
#define PIN_LCD_D5 46
#define PIN_LCD_D6 47
#define PIN_LCD_D7 48
#define I2S_BCLK 12
#define I2S_LRC 11
#define I2S_DOUT 13

#define PIN_POWER_ON 15

#define PIN_LCD_RES 5
#define PIN_LCD_CS 6
#define PIN_LCD_DC 7
#define PIN_LCD_WR 8
#define PIN_LCD_RD 9

#define PIN_BUTTON_1 0
#define PIN_BUTTON_2 14
#define PIN_BAT_VOLT 4

#define PIN_IIC_SCL 17
#define PIN_IIC_SDA 18

#define PIN_TOUCH_INT 16
#define PIN_TOUCH_RES 21
