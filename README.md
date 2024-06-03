# Car_Plate_Detection_OCR

## 1. 자동차 번호판 번호 및 글자 인식

## 2. Dataset: 
Korea Car License Plate Image Dataset URL(https://universe.roboflow.com/hyunjin/korea-car-license-plate/dataset/2)

## 3. Data Preprocessing

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

## 4. Methods:
   ### 4-1) Object Detection Model: YoloV9c
   ![image](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/00ba1601-3c34-42bd-92c9-d0a80e6af7d2)

   ![스크린샷 2024-06-03 오후 9 53 49](https://github.com/ssuzzang/Car_Plate_Detection_OCR/assets/97435321/62415ef7-fa7b-4bf4-abd7-0492c1ede8c8)

   ### 4-2) OCR Method: Easy OCR
   

## 5. Post processing:

동영상 프레임별 번호판 인식 및 OCR 인식




## 6. Reference:
1. YoloV9: https://docs.ultralytics.com/ko/models/yolov9/
