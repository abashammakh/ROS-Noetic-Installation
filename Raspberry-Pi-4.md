# <div dir="rtl">تثبيت ROS على الراسبيري باي 4</div>

## <div dir="rtl">المتطلبات</div>
<div dir="rtl"><ul>
  <li>Micro-HDMI الى HDMI</li>
  <li>USB type-c</li>
  <li>Ethernet كابل</li>
  <li>لوحة مفاتيح</li>
  <li>Micro-SD Card (يفضل 8 جيجا)</li>
</ul></div>

- [Raspberry Pi Imager](https://www.raspberrypi.org/downloads/)

## <div dir="rtl">خطوات التثبيت</div>

### <div dir="rtl">1.1 وصل الذاكرة وثبت أوبونتو 20.04 نسخة الخادم 64-bit</div>
<div dir="rtl"><ul>
  <li>1. أختار نظام التشغيل</li>
  <li>2. اختار الذاكرة</li>
  <li>3. أضغط على WRITE</li>
</ul></div>

![](images/6.jpg)

![](images/7.jpg)

![](images/8.jpg)

### <div dir="rtl">1.2 وصل الذاكرة للجهاز بالاضافة لكابل الشبكة ولوحة المفاتيح وسلك الطاقة.</div>

### <div dir="rtl">1.3 قم بتسجيل الدخول باستخدام البيانات التالية</div>
<div dir="rtl">أسم المستخدم: ubuntu</div>
<div dir="rtl">كلمة المرور: ubuntu</div>


### <div dir="rtl">1.4 قم بكتابة الاوامر التالية لتثبيت ROS</div>

**<div dir="rtl">ملاحظة: هذه النسخة هيا النسخة البدائية ولا تحتوي على أي ادوات ذات واجهة رسومية.</div>**

> sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

> sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

> sudo apt update

> sudo apt install ros-noetic-ros-base

> echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

> source ~/.bashrc

<div dir="rtl">1.5 للتأكد بأن التثبيت تم بنجاح قم بكتابة الامر التالي</div>

> rosversion --distro

<div dir="rtl">سيتم طباعة الكلمة التالية</div>

> noetic

![](images/9.jpg)

## <div dir="rtl">المصادر</div>

[<div dir="rtl">Raspberry Pi</div>](www.raspberrypi.org)
[<div dir="rtl">ROS Official Website</div>](https://www.ros.org/)

---

# ROS Installation on Raspberry Pi 4

## Requirements
- Raspberry Pi 4
- Micro-HDMI to HDMI
- USB type-c power cable
- Ethernet cable
- Keyboard
-  (8 GB recommended)
- [Raspberry Pi Imager](https://www.raspberrypi.org/downloads/)

## Installation Steps

### 1.1 Connect the Micro-SD card and install Ubuntu 20.04 Server 64-Bit
1. Select the OS
2. Select the Micro-SD Card
3. Click WRITE

![](images/6.jpg)

![](images/7.jpg)

![](images/8.jpg)

### 1.2 After writing the image to the memory card. Connect it to the Pi, also connect the ethernet and keyboard and power cable.

### 1.3 Login to pi using the following credentials
> Username: ubuntu
> 
> Password: ubuntu

After entring the credentials, The OS will ask you to change the password.

### 1.4 Run the following commands to install ROS (ROS-Base\Bare Bones)
> **Note: We are installing the ROS-Base Version (CLI only, No GUI tools.)**

> sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

> sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

> sudo apt update

> sudo apt install ros-noetic-ros-base

> echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

> source ~/.bashrc

### 1.5 Run the following command to check if ROS installed successfully.

> rosversion --distro

The output should be

> noetic

![](images/9.jpg)

## Resource
- [Raspberry Pi](www.raspberrypi.org)
- [ROS Official Website](https://www.ros.org/)
