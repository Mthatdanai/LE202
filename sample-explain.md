# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

    #include <Arduino.h>        							.ดึงข้อมูลมาจาก Arduino.h
    
    int cnt = 0;               							        .จำนวนเต็มเริ่มนับจาก 0
    
    void setup()              						                .ส่วน set up เริ่มต้นของโปรแกรม 
    {
     	Serial.begin(115200);                                                           .ตั้งค่าความเร็วในการสื่อสารเป็นบิตต่อวินาที
    }

    void loop()                                                                         .บอกโปรแกรมวนรูปโค้ดข้างล่าง
    {
	    cnt++;									.นับเพิ่มทีละ 1
	    Serial.printf("PATTANI :%d\n",cnt);						.แสดงผลข้อมูล  นับจำนวน
	    int s = cnt % 5 + 1;							.ให้ s เก็บค่าจำนวนเต็มจากผลคำนวณ
	    int d = s * 1000;								.ให็ d เก็บค่าจำนวนเต็มดีเลย์จากการคำนวณ
	    delay(d);								        .แสดงค่าดีเลย์
    }	

# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ

		#include <Arduino.h> 							.ดึงข้อมูลมาจาก Arduino.h
		#include <ESP8266WiFi.h>						.ดึงข้อมูลมาจาก ESP8266WiFi.h

		int cnt = 0;								.จำนวนเต็มเริ่มนับจาก 0

		void setup()								.ส่วนset up เริ่มต้นของโปรแกรม
		{
			Serial.begin(115200);						.ตั้งค่าความเร็วในการสื่อสารเป็นบิตต่อวินาที
			WiFi.mode(WIFI_STA);						.ตั้งค่า wifi เป็นโหมดสถานี
			WiFi.disconnect();						.ตัดการเชื่อมต่อ wifi ก่อนหน้า
			delay(100);							.ค่าดีเลย์
			Serial.println("\n\n\n");					
		}

		void loop()								.บอกโปรแกรมวนรูปโค้ดข้างล่าง
		{
			Serial.println("========== เริ่มต้นแสกนหา Wifi ===========");      .แสดงผลข้อมูล
			int n = WiFi.scanNetworks();					.แสกนหา wifi
			if(n == 0) {							.หากหาไม่พบ
				Serial.println("NO NETWORK FOUND");			.แสดงผลว่าไม่พบสัญญาณ wifi
			} else {							.ถ้าเป็นกรณีพบสัญญาณ
				for(int i=0; i<n; i++) {
					Serial.print(i + 1); 				
					Serial.print(": ");
					Serial.print(WiFi.SSID(i));			.แสดงชื่อสัญญาณ
					Serial.print(" (");
					Serial.print(WiFi.RSSI(i));			.แสดงความเร็วของสัญญาณ
					Serial.println(")");
					Serial.print(WiFi.channel(i));			.แสดง channel ของสัญญาณ
					delay(10);					
				}
			}
			Serial.println("\n\n");
			delay(10 * 1000);
		}	

# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล

		#include <Arduino.h>							.ดึงข้อมูลมาจาก Arduino.h
		#include <ESP8266WiFi.h>						.ดึงข้อมูลมาจาก ESP8266WiFi.h

		int cnt = 0;								.จำนวนเต็มเริ่มนับจาก 0

		void setup()								.ส่วน set up เริ่มต้นของโปรแกรม
		{
			Serial.begin(115200);						.ตั้งค่าความเร็วในการสื่อสารเป็นบิตต่อวินาที
			pinMode(0, OUTPUT);						.กำหนดการทำงานของ pin
			Serial.println("\n\n\n");
		}

		void loop()								.บอกโปรแกรมวนรูปโค้ดข้างล่าง
		{
			cnt++;								.นับเพิ่มทีละ 1
			if(cnt % 2) {							.ถ้าค่าที่นับได้หารสองเหลือเศษ 0
				Serial.println("========== ON ===========");		.แสดงผลว่า on
				digitalWrite(0, HIGH);    				.ใช้สำหรับสั่งให้ Arduino เขียนค่า HIGH ที่ขา digital ของบอร์ด
			} else {
				Serial.println("========== OFF ===========");		.ถ้าค่าที่นับได้หารสองเหลือเศษ 1
				digitalWrite(0, LOW);					.ใช้สำหรับสั่งให้ Arduino เขียนค่า HIGH ที่ขา digital ของบอร์ด
			}
			delay(500);							.แสดงผลดีเลย์
		}

# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล

		#include <Arduino.h>							.ดึงข้อมูลมาจาก Arduino.h
		#include <ESP8266WiFi.h>						.ดึงข้อมูลมาจาก ESP8266WiFi.h

		int cnt = 0;								.จำนวนเต็มเริ่มนับจาก 0

		void setup()								.ส่วน set up เริ่มต้นของโปรแกรม
		{
			Serial.begin(115200);
			pinMode(0, INPUT);
			pinMode(2, OUTPUT);
			Serial.println("\n\n\n");
		}

		void loop()
		{
			int val = digitalRead(0);
			Serial.printf("======= read %d\n", val);
			if(val==1) {
				digitalWrite(2, LOW);
			} else {
				digitalWrite(2, HIGH);
			}
			delay(100);
		}

# การทดลองที่ 5 เรื่อง การเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์

		#include <ESP8266WiFi.h>
		//#include <WiFiClient.h>
		#include <ESP8266WebServer.h>

		const char* ssid = "HI_BMFWIFI_2.4G";
		const char* password = "0819110933";

		ESP8266WebServer server(80);

		int cnt = 0;

		void setup(void){
			Serial.begin(115200);

			WiFi.mode(WIFI_STA);
			WiFi.begin(ssid, password);
			while (WiFi.status() != WL_CONNECTED) {
				delay(500);
				Serial.print(".");
			}
			Serial.print("\n\nIP address: ");
			Serial.println(WiFi.localIP());

			server.onNotFound([]() {
				server.send(404, "text/plain", "Path Not Found");
			});

			/// http://192.0.0.1/ = Hello cnt: ???
			server.on("/", []() {
				cnt++;
				String msg = "Hello cnt: ";
				msg += cnt;
				server.send(200, "text/plain", msg);
			});
			/// http://192.0.0.1/on = Hello cnt: ???
			server.on("/on", []() {
				cnt++;
				String msg = "Switch on ";
				msg += cnt;
				server.send(200, "text/plain", msg);
			});
			/// http://192.0.0.1/off = Switch off: ???
			server.on("/off", []() {
				cnt++;
				String msg = "Hello cnt: ";
				msg += cnt;
				server.send(200, "text/plain", msg);
			});

			server.begin();
			Serial.println("HTTP server started");
		}

		void loop(void){
		server.handleClient();
		}

# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

		#include <ESP8266WiFi.h>
		//#include <WiFiClient.h>
		#include <ESP8266WebServer.h>

		const char* ssid = "MY-ESP8266";
		const char* password = "choompol";

		IPAddress local_ip(192, 168, 1, 1);
		IPAddress gateway(192, 168, 1, 1);
		IPAddress subnet(255, 255, 255, 0);

		ESP8266WebServer server(80);

		int cnt = 0;

		void setup(void){
			Serial.begin(115200);

			WiFi.softAP(ssid, password);
			WiFi.softAPConfig(local_ip, gateway, subnet);
			delay(100);

			server.onNotFound([]() {
				server.send(404, "text/plain", "Path Not Found");
			});

			server.on("/", []() {
				cnt++;
				String msg = "Hello cnt: ";
				msg += cnt;
				server.send(200, "text/plain", msg);
			});

			server.begin();
			Serial.println("HTTP server started");
		}

		void loop(void){
  		server.handleClient();
		}
