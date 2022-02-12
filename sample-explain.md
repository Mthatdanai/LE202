# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

    #include <Arduino.h>
    
    int cnt = 0;
    
    void setup()
    {
     	Serial.begin(115200);
    }

    void loop()
    {
	    cnt++;
	    Serial.printf("PATTANI :%d\n",cnt);
	    int s = cnt % 5 + 1;
	    int d = s * 1000;
	    delay(d);
    }	

# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ


