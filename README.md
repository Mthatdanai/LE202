# ความรู้ทั่วไป

## Digital

ข้อมูลดิจิตอลคือการเอาสัญญาณไฟฟ้ามาแทนด้วยตัวเลข และตัวเลขเหล่านี้เรียกว่า Digital Binary เป็นเลขฐานสอง คือมีแค่ 0 กับ 1 เช่นให้สัญญาณonคือ1 สัญญาณ off คือ 0 เป็นต้น นอกจากนี้เราสามารถใช้ระบบเลขฐานแทนตัวอักษรเช่นถ้าเป็นภาษาอังกฤษจะใช้เลขฐาน 8 ถ้าเป็นภาษาไทยจะใช้เลขฐาน16

## Voltage

แรงดันไฟฟ้าคือความต่างศักดิ์ระหว่างจุดสองจุดซึ่งสามารถวัดได้มีหน่วยเป็นโวลต์ แรงดันไฟฟ้ามี 2 ประเภทคือ แรงดันไฟฟ้าประแสตรง และแรงดันไฟฟ้ากระแสสลับ ตัวอย่างแรงดันไฟฟ้าที่อยู่รอบตัวเช่น ไฟบ้าน เครื่องคอมพิวเตอร์ โทรศัพท์มือถือเป็นต้น

## Computer

คอมพิวเตอร์มีพัฒนาการมานานเมื่อ 50 – 60 ปีที่แล้ว คอมพิวเตอร์ยุคแรกๆจะมีขนาดใหญ่เท่ากับอาคารชั้นหนึ่ง และมีขนาดเล็กลงมาเรื่อย ๆ เท่ากับที่ใช้ปัจจุบันและเล็กสุดคือคอมพิวเตอร์ตัวจิ๋วที่ใช้ในการเชื่อมอินเตอร์เน็ต ความเร็วของคอมพิวเตอร์ก็มีมากขึ้นเรื่อย ๆ และยังสามารถเชื่อมโยงกันด้วยอินเตอร์เน็ตความเร็วสูง

## Internet

อินเตอร์เน็ตสามารถเชื่องโยงสิ่งต่างๆได้เช่นมือถือ ทีวี คอมพิวเตอร์ เว็บไซต์ต่างๆ ทั้งแบบมีสายและไร้สายเชื่อมโยงได้ทั่วโลก โดยเชื่อมโยงผ่าน wi-fi Bluetooth airdrop เป็นต้น ในปัจจุบันมีผู้ใช้อินเตอร์เน็ตมากกว่า 4800ล้านคน และมีเว็บไวต์ที่เปิดมาแล้วกว่า1800ล้านเว็บไซต์

## Program language

การพัฒนาการเขียนซอฟแวร์ให้รันบนคอมพิวเตอร์มีพัฒนาการมาอย่างยาวนาน เมื่อ 50- 70 ปีที่แล้ว เริ่มต้นจากภาษาAssembly และ ภาษาC ต่อมามีภาษาที่พัฒนามาจำนวนมาก เช่นภาษาJava ภาษาPythonอื่นๆอีกมากมาย ภาษาถูกพัฒนาให้คนเขียนภาษาได้ง่ายขึ้น พัฒนาโปรแกรมได้ง่ายขึ้น

## Platformio

PlatformIO เป็น Open source software สําหรับพัฒนา Embedded หรือพัฒนา IoT ได้ในแบบ Cross-platform หมายความว่า PlatformIO จะช่วยให้เราสามารถพัฒนาโปรแกรมสําหรับ Embedded ตระกูล ใดๆก็ได้ เช่น Arduino, ESP8266, EMBED ฯลฯ

# ตัวอย่างการทดลอง

### โปรแกรมตัวอย่างที่1
เป็นการลงโปรแกรมด้วยแพลตฟอร์ม io โหลดไปยัง supercomputerตัวจิ๋ว นั่นคือไมโครคอนโทรลเลอร์ ESP-01 แล้วดูผลลัพธ์ที่เป็นการนับเลขอย่างไม่รู้จบ

### โปรแกรมตัวอย่างที่2 
เป็นการใช้ไมโครคอนโทรลเลอร์ ESP-01ที่มีไวไฟ มีset up สองส่วนคือส่วนไวไฟและวนลูป โดยแสดงผลว่าเริ่มต้นค้นหาไวไฟ แล้วแสดงผลว่าไวไฟรอบตัวมีอะไรบ้าง

### โปรแกรมตัวอย่างที่3
เป็นโปรแกรมที่ให้รันบนไมโครคอนโทรลเลอร์ ESP-01 เป็นโปรแกรมที่ให้ทดลองการเอาท์พุตสัญญาณออกไปภายนอก โดยเสียบอแดปเตอร์ต่อระหว่าง USB to serial กับ คอมพิวเตอร์ โดยอแดปเตอร์จะส่งสัญญาณไปที่พอร์ต 0 และ พอร์ต 2 ที่ต่อกับไฟLED หลังจากอัพโหลดโปรแกรมแล้วทำการรันโปรแกรม จะสังเกตเห็นหลอดไฟLEDกระพริบ

### โปรแกรมตัวอย่างที่4  
เป็นการนำอินพุตจากภายนอกเข้ามาในไมโครคอนโทรลเลอร์ โปรแกรมจะทำงานโดยตรวจสอบที่พอร์ต 0ว่ามีอินพุตเข้ามาหรือไม่ ถ้าอินพุตเป็น 1 จะติดไฟที่พอร์ต 2 ถ้าเป็น 0 จะไม่ติดไฟ จากนั้นเช็คที่ monitor ได้ค่าอินพุตเป็น 1 ตลอด ซึ่งไฟจะไม่ติด ถ้าต่อพอร์ต 0 เข้าไป อินพุตจะกลายเป็น 0 ไฟจะติด จากนั้นนำเซนเซอร์ที่ต่ออยู่กับตัวต้านทานต่อเข้ากับไฟเลี้ยง ใส่ไฟเข้า 3 โวลต์แล้วนำเซนเซอร์ต่อเข้ากับพอร์ต 0 อีกขาต่อเข้ากับกราวน์ จากนั้นทำการสังเกตจะเห็นว่าเมื่อเซนเซอร์รับแสง หลอดไฟLEDจะติด ค่าอินพุตเป็น0 ถ้าบังเซนเซอร์หลอดไฟLEDจะดับ ค่าอินพุตเป็น 1

### โปรแกรมตัวอย่างที่5 
คือโปรแกรมที่สร้างเว็บserverผ่านไวไฟ โปรแกรมส่วนแรกเป็นการรับwifi ที่เลือก ส่วนที่สองเป็นส่วนเว็บserverของเรา เราจะทำการต่อไมโครคอนโทรลเลอร์เข้ากับ USB to serial แล้วทำการอัพโหลดโปรแกรมเข้าไมโครคอนโทรลเลอร์ เนื่องจากโปรแกรมของเราคือเว็บserver เราจะทำการทดสอบโดยใช้เว็บบราวน์เซอร์ทั่วไปได้

### โปรแกรมตัวอย่างที่6 
โปรแกรมนี้คล้ายกับโปรแกรมตัวอย่างที่5 แต่แตกต่างตรงที่โปรแกรมที่5เชื่อมกับwifiที่มีอยู่แล้วแต่โปรแกรมนี้สร้างwifi access ขึ้นมาเองเพื่อสามารถเชื่อมต่อแบบไร้สายได้ จากนั้นเราสามารถทดสอบโดยใช้โทรศัพท์มือถือ หรือ คอมพิวเตอร์เข้ามาเชื่อมต่อกับ wifi acess ตัวนี้
