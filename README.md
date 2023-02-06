# Fork สิ รอ***ไรหล่ะ
ข้อนี้เป็นไปตามโจทย์ใน google doc ที่พี่ทิ้งไว้ให้ ซึ่งตัวนี้เป็นแค่ template ที่เอาไว้ให้เฉยๆ หากน้องมีแนวทางการเขียนโค้ดแบบไหนก็ปรับเปลี่ยนได้เลยตามใจชอบ ขอแค่ผลลัพธ์ถูกต้องตามโจทย์ก็เพียงพอ

ในทางที่ดีงานนี้ควรแบ่งทำกัน 2 คน คือ
- คนเขียนฟังก์ชันในการ GET POST (ใน src -> traffic.h)
- คนเขียน state ต่างๆ (ใน src -> main.cpp)

โค้ดเขียนไว้บางส่วนแล้ว สามารถเติมเพิ่มตรง 
``` c
// *** write your code here ***
```
และทำการแก้ค่าตัวแปร ก็เพียงพอที่จะทำโจทย์สำเร็จแล้ว

## Connect_Wifi()
กรุณาไปเติมโค้ดให้ครบด้วย
``` c
// src/main.cpp
const char *ssid = "Galaxy A30C9C8";
const char *password = "himl9080";
```

## Define
ไปเปลี่ยนตาม pin ที่น้องต่อด้วย
``` c
// src/main.cpp
#define red 26
#define yellow 25
#define green 33
#define ldr 34
#define button 27

#define light 0
```

## Point
ไปเปลี่ยนตาม point ของเราด้วย (point == กลุ่มที่)
``` c
// src/traffic.h
const String point = "5";
const int nearby_1 = 3;
const int nearby_2 = 5;
```

## GET_traffic
อยู่ใน `src/traffic.h`

จะขาดส่วน แสดงผล ซึ่งอาจจะต้องใช้ `JsonArray`, `JsonObject`, `JsonPair` (แล้วแต่กลุ่มเลย บางกลุ่มอาจไม่ต้องใช้ก็ได้)

สามารถดูตัวอย่างและนำมาปรับใช้ได้จาก[ที่นี่](https://stackoverflow.com/questions/71023794/getting-json-keys-from-an-array-from-an-object-using-arduinojson)

## POST_traffic
อยู่ใน `src/traffic.h`

แทบไม่ต่างจากในตัวอย่างเลย เพิ่มเติมคือมันจะรับตัวแปร `String led` ที่เป็นตัวบอกว่า led ตอนนี้สีอะไร ดังนั้นน้องเหลือแค่เติมการใส่ข้อมูลลง `doc` ให้ถูกต้องก็เพียงพอ

เวลานำไปใช้งานก็จะใช้ เช่น `POST_traffic("green");` เพื่อ POST บอกว่าตอนนี้สีเขียวนะ (ทั้งนี้ก็แล้วแต่การออกแบบของแต่ละกลุ่ม เปลี่ยนแปลงได้เลยตามใจชอบ)

## void loop
อยู่ใน `src/main.cpp`
พี่ออกแบบเป็นการทำ state 1 2 3 (แต่ละอันแทนอะไรลองคิดเอานะครับ)

ทั้งนี้น้องๆสามารถเปลี่ยนแปลงได้ตามใจชอบเลย อาจไม่ใช้ state ก็ได้เช่นกัน

# DOC
[Google Doc](https://docs.google.com/document/d/1WDnPvVdG5Sv5STsbMxcOpFad4R2GMMGk-eMUh6Ukz0c/edit?usp=sharing)