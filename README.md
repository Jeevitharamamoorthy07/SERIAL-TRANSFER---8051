# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
OUTPUT:
<img width="1026" height="347" alt="Screenshot 2025-11-02 205930" src="https://github.com/user-attachments/assets/26578f05-7f67-4983-bd3d-772c481b2bf1" />
<img width="823" height="339" alt="Screenshot 2025-10-29 094215" src="https://github.com/user-attachments/assets/1986f3a3-53a5-4db5-949c-bec18cf5591b" />



**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
