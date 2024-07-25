# การสร้าง project ของ ESP32

องค์ประกอบสำหรับโปรเจคของ ESP32 ประกอบด้วย source code และไฟล์จำนวนหนึ่ง ที่ทำหน้าที่เป็นตัวกำกับเครื่องมือช่วยสร้าง project  ให้สามารถทำงานได้
โดยมีโครงสร้างของโฟลเดอร์สำหรับโปรเคดังนี้

![รูปภาพ1](Pictures/รูปภาพ1.png)

ภายใน componnet Main จะมีไฟล์ source code และไฟล์ CMakeLists.txt ไว้สำหรับการสร้าง component เช่นเดียวกัน

![รูปภาพ2](Pictures/รูปภาพ2.png)

## 1. สร้าง folder สำหรับ project

### 1.1  เปิด VSCODE แล้ว สร้าง folder  ใหม่เพื่อสร้าง  project

1.1.1 เรียกเมนู file --> Open Folder... 

![alt text](Pictures/image.png)

1.1.2 browse ไปที่ folder ที่จะเก็บโปรเจค แล้วสร้าง folder  ใหม่ ในที่นี้ชื่อ ESP32_Blank

![alt text](Pictures/image-1.png)

1.1.3 สร้างไฟล์ใหม่ ตั้งชื่อ  Makefile และเพิ่มเนื้อหาดังนี้

![alt text](Pictures/image-2.png)

เนื้อหาใน Makefile

``` makefile
#
# This is a project Makefile. It is assumed the directory this Makefile resides in is a
# project subdirectory.
#

PROJECT_NAME := app-template

include $(IDF_PATH)/make/project.mk
```

1.1.4 สร้างไฟล์ใหม่ ตั้งชื่อ  CMakeLists.txt และเพิ่มเนื้อหาดังนี้

![alt text](Pictures/image-3.png)

``` CMake
# The following lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(app-template)
```


## 2. สร้าง folder สำหรับ component Main
### 2.1 สร้าง folder  ใหม่สำหรับ component Main 

1.2.1 สร้าง folder main

![alt text](Pictures/image-4.png)


1.2.2 เพิ่มไฟล์ main.c

![alt text](Pictures/image-6.png)




## 3. ทดสอบรัน project
