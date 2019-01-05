---
title : CoCo_version_decument(ver 1.0.0) 
writer : khosungpil
type : Version document(official)
local : soma05
objective : 로컬에서 버전을 업데이트하고 변경 사항 있을 시 문서화 한다.
---

# CoCo version Document #

## ver 1.0.0 (2018.12.17) ##
1. 공식 메뉴얼 작성
2. 필요한 코드만 남기고 전부 백업
<hr>

## ver 1.0.1 (2018.12.21) ##
1. extract_part_1220.py, 이미지 전처리 코드 수정
    - 사진 리사이징 640:480으로 고정
    - segment 리사이징 할 시 확대 리사이징 코드 삭제
    - 변수명 및 함수명 변경
2. image_preprocessing.py
    - Import 변경, 함수 변경

## ver 1.0.2 (2018.12.26) ##
1. post_process_debugging.py, 이미지 후처리 logic 구현
    - 기존의 coarse_mask만으로 상의 영역을 잘랐음.
    - binary_segment만으로 상의 영역을 자르면 기존 이미지 영역에 제한됨.
    - coarse_mask + binary_segment라는 final_mask를 통해 보완
    - 옷 주위를 하얀 Line으로 구성, 하지만 전의 옷이 조금 남아있는 경우도 생김
2. 1115_final.py에 이식해야 함.

## ver 1.0.3 (2019.01.05) ##
1. doc_imagepreprocessing.md 전체 수정해야 함.
2. register_product
    - flask server에서 요청이 오면 상품이 등록할 수 있도록 변경
    - 추후에 상품 이미지 사이즈를 고려하여 4:3 비율로 떨어지도록 해야함. 그렇지 않으면 상품 이미지가 변형될 여지가 있음.