---
title: Psd 블렌딩 옵션 조작
weight: 100
type: docs
description: Aspose.PSD for Java를 사용하면 간단한 코드 스니펫으로 블렌딩 옵션을 조정할 수 있습니다.
keywords: [블렌드 옵션, 블렌딩, 효과 추가, 불투명도 변경, 그림자 색상 변경, 그림자 추가, psd api, java, 코드 샘플]
url: ko/java/blending-options/
---

## **개요**
Aspose.PSD for Java를 사용하면 PSD 이미지 내 레이어의 외관을 향상시키기 위해 블렌딩 옵션을 수정할 수 있습니다. 아래는 블렌딩 옵션을 활용하는 다양한 방법을 설명하는 Java 코드 예제입니다.

먼저, 코드는 PSD 이미지를 로드하여 원본 PNG 파일로 저장합니다. 그런 다음 특정 레이어의 불투명도와 블렌딩 모드를 변경합니다. 예를 들어, 두 번째 레이어의 불투명도를 100으로 설정하고 다섯 번째 레이어의 블렌딩 모드를 Hue로 변경합니다.

또한 코드는 지정된 레이어에 블렌딩 효과를 통합합니다. `addDropShadow()` 메서드를 사용하여 일곱 번째 레이어에 그림자 효과를 도입하며, 30도의 그림자 각도와 RGB(255, 0, 0) 그림자 색상을 지정합니다.

또 다른 코드는 아홉 번째 레이어의 블렌딩 모드를 Lighten으로 조정합니다. 또한, 다섯 번째 레이어에 `addColorOverlay()` 메서드를 통해 색상 오버레이 효과를 적용하며, 이를 RGB(30, 50, 0) 색상 오버레이로 설정하고 불투명도를 150으로 지정합니다.

마지막으로, 코드는 수정된 이미지를 업데이트된 PNG 파일로 저장합니다.

본질적으로 Aspose.PSD for Java는 PSD 이미지 내 레이어의 외관을 조작하기 위한 다양한 블렌딩 옵션을 제공합니다. 이러한 옵션에는 불투명도 수정, 블렌딩 모드 변경 및 드롭 쉐도우 및 색상 오버레이와 같은 다양한 블렌딩 효과의 적용이 포함됩니다.

## **예시**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-blending-options.java" >}}
