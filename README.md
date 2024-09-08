# opencvMisson
opencv 이미지 필터 AI 수강 미션

# 미션1: 색감 노이즈 필터링 + 선명도
## 사용한 메서드: <code>fastNlMeansDenoisingColored</code>, <code>filter2D (sharpen kernel)</code>
### <code>cv2.fastNlMeansDenoisingColored</code>
각 픽셀 주의에 유사한 픽셀들과 평균을 내서 잡음을 제거
### <code>cv2.filter2D (sharpen kernel)</code> 
주변 픽셀과 값을 극대화 해서 이미지 선명도를 높임
![01](https://github.com/user-attachments/assets/3c136e0b-96ef-4d9b-b2d9-ba9d5b7acb13)
#### 1. (Denoise) 원본 이미지에 Denoise 효과 적용
![misson1_1denoise](https://github.com/user-attachments/assets/a0e52c78-14fb-4a04-a403-0a921ce2cf68)
#### 2. (Denoise with Mask) 마스크를 씌워 밝은 곳에만 denoise 효과 적용
![misson1_2denoise+mask](https://github.com/user-attachments/assets/a810225f-ac2f-48ad-aa58-c19589ba5343)
#### 3. (Denoise with Mask, then sharpen) 마자막으로 이미지의 선명도 높여 출력한다
![misson1_so](https://github.com/user-attachments/assets/3ca280fa-0032-41d8-936d-7b66092c7747)

# 미션2: 밝기 조절
## 사용한 메서드: <code>np.clip</code>
### <code>np.clip</code>
지정 한 최저값보다 작고나 혹은 지정한 최대값보다 큰 값들을 각각 최저와 최대값으로 대체해서 전체적으로 디밍(dimming)효과를 주기
![03](https://github.com/user-attachments/assets/1a402ad8-a15c-4040-a6d2-a0ee3a1ecac3)
![misson2_so](https://github.com/user-attachments/assets/e5d0dd2b-efd3-4099-8975-92261f7e7ad9)

# 미션3: 대비 효과
## 사용한 메서드: <code>cv2.convertScaleAbs</code>
### <code>cv2.convertScaleAbs</code>
밝기와 대비를 기존 픽셀에 각각 곱하고 더해 대비 효과를 세부적으로 조정 할 수 있다 (어두운 곳은 더 어둡게, 밝은 곳은 더 밝게)
![05](https://github.com/user-attachments/assets/da65473d-f152-4c05-b8b7-abcbce5ea37b)
![misson3_so](https://github.com/user-attachments/assets/596ebefa-daeb-404c-800d-b85a605b5086)

