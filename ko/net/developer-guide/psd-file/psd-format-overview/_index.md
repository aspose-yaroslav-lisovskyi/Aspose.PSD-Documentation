---
title: PSD 형식 개요
type: docs
weight: 60
url: /ko/net/psd-format-overview/
---

## **설명**
PSD는 Adobe Photoshop의 그래픽 디자인 및 개발에 사용되는 네이티브 파일 형식인 Photoshop 문서를 나타냅니다.

## **파일 형식 명세**
PSD 파일의 데이터는 빅 엔디안 바이트 순서로 저장됩니다. 이는 Windows 플랫폼에서 읽거나 쓸 때 short 및 long 정수를 교체해야 함을 의미합니다. Photoshop 파일 형식은 다섯 가지 주요 부분으로 나뉩니다. 각 섹션으로 이동하는 데 사용할 수 있는 많은 길이 표시기가 있습니다. 길이 표시기는 일반적으로 가장 가까운 2 또는 4바이트 간격으로 반올림되도록 바이트로 패딩됩니다. 다섯 가지 주요 부분은 다음과 같습니다:

- 파일 헤더
- 색 모드 데이터
- 이미지 리소스
- 레이어 및 마스크 정보
- 이미지 데이터

일관성을 유지하기 위해 Photoshop은 모든 이 섹션에 대해 데이터를 써야 할 수 있습니다. 파일에 쓸 때 무시된 필드에는 0을 써야 한다는 것을 의미하기도 합니다. 길이 지정된 섹션의 길이 필드는 읽기를 중지할 시기를 결정하는 데 사용해야 합니다. 대부분의 경우, 길이 필드는 레코드가 아닌 바이트 수를 나타냅니다. 파일을 읽을 때 다음 사항을 기억해야 합니다.

- 모든 표의 "길이" 열에 정의된 값은 바이트 단위입니다.
- Unicode 문자열로 정의된 모든 값은 다음과 같이 구성됩니다:
  - 문자열의 문자 수를 나타내는 4바이트 길이 필드(바이트가 아님).
  - 문자당 두 바이트인 유니코드 값의 문자열.

## **형식의 특징**
PSD 파일에는 이미지 레이어, 조정 레이어, 레이어 마스크, 주석, 파일 정보, 키워드 및 기타 Photoshop 특정 요소가 포함될 수 있습니다. Photoshop 파일의 기본 확장명은 .PSD이며 이미지의 최대 높이와 너비는 30,000 픽셀이며 길이 제한은 2 기가바이트입니다.

## **사용 방법**
1. PSD 슬라이싱 도구.
1. HTML로의 [PSD 변환](/psd/ko/net/converting-psd-image-to-raster-format/).
1. 이메일에 대한 [템플릿으로서의 PSD 사용](/psd/ko/net/using-psd-files-as-templates-for-automation-business-cards-case/).
1. 특정 CMS HTML로의 PSD 변환.
1. PSD 파일에서의 아이덴티켓(경찰 스케치).
1. 병, 컵, 티셔츠 등과 같은 상품을 위해 스마트 객체를 사용하여 의사 3D 미리보기 이미지 생성.
1. PSD의 빠른 편집: 자동 톤, 프리셋, 스마트 객체, 텍스트 레이어 이미지 자르기.

그리고 더 많은 기능이 있습니다. Aspose.PSD를 사용하여 멋진 작업을 완성했다면, [Aspose 포럼](https://forum.aspose.com/)에서 케이스 스터디를 공유해 주세요.

추가 예시는 다음에서 확인할 수 있습니다:

- [케이스 스터디](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [쇼케이스](/psd/ko/net/showcases-html/)