# Car_Plate_Detection_OCR

# 프로젝트 명: 자동차 번호판 번호 및 글자 인식

## 1. 기간: 2024.05 ~ 06

## 2. Skills: 
### Opencv, Easyocr, Roboflow, Ultralytics, Numpy ,Maplotlib, Regular Expression

## 3. Dataset: 
Korea Car License Plate Image Dataset URL(https://universe.roboflow.com/hyunjin/korea-car-license-plate/dataset/2)

## 4. Data Preprocessing

### Image:
1) Resize: 640 x 640
2) Flip: Horizontal, Vertical
3) 90° Rotate: Clockwise, Counter-Clockwise, Upside Down
4) Crop: 0% Minimum Zoom, 20% Maximum Zoom
5) Rotation: Between -15° and +15°
6) Shear: ±15° Horizontal, ±15° Vertical

### Example:

![image](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/3c120df8-eb11-4aba-beb9-db7e4e484f5f)
![image](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/ace7389c-c5c0-4375-9f26-67031fcc6826)

## 5. Methods:
   ### 5-1) Object Detection Model: YoloV9c
   ![image](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/00ba1601-3c34-42bd-92c9-d0a80e6af7d2)


   ### train batch:
   ![image](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/4c3876ec-b35d-48d1-9712-341b9a634b9e)


   ![스크린샷 2024-06-03 오후 9 53 49](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/62415ef7-fa7b-4bf4-abd7-0492c1ede8c8)

   ### 5-2) OCR Method: Easy OCR
   

## 6. Post processing:

동영상 프레임별 번호판 인식 및 OCR 인식

## 7. Result:



## 8. 고찰:
자동차가 정면에서가 아닌 측면에서 있을때 바운딩 박스내에 많은 공간을 포함하여 번호판을 인식하는 것으로 파악되었고, 이를 통해 OCR 성능이 저하되는것을 볼 수 있었다.
그로인해 숫자와 글자 인식 성능을 높이기 위하여 자동차가 화면 중앙에 있을때 인식할 수 있도록 조건문을 만들었고, 번호판 규칙을 통해 가운데에 문자가 있고 앞뒤로 숫자가 있는 신형 번호판의 규칙을 정규 표현식으로 검증하는 조건문을 만들어서
정확히 인식될때만 출력할 수 있도록 조건을 취하였다.

![스크린샷 2024-06-03 오후 10 09 26](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/9964c2d0-7e19-4ed5-89aa-e63b6cedb3cb)



## 8. Reference:
1. YoloV9: https://docs.ultralytics.com/ko/models/yolov9/
