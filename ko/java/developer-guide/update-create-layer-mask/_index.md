---
title: Aspose.PSD for Java에서 마스크 작업하기
weight: 100
type: docs
description: PSD 파일 내의 클리핑, 래스터 및 벡터 마스크 작업 예제
keywords: [마스크, 레이어 마스크, 벡터 마스크, 클리핑 마스크, psd, psd api, java, 코드 샘플]
url: ko/java/update-create-layer-mask/
---

## **개요**

**개요**
	
	PSD 파일에는 3 가지 유형의 마스크가 있습니다:
	1. 클리핑 마스크
	2. 래스터 마스크
	3. 벡터 마스크
	
	이 기사에서는 이 3가지 유형을 모두 다루겠습니다.


** 클리핑 마스크 **

클리핑 마스크는 그래픽 디자인 및 이미지 편집 소프트웨어에서 강력한 기능 중 하나이며 특히 Java에서 중요합니다. 이들은 다른 레이어의 모양과 내용에 기초하여 한 레이어의 가시성을 정확하게 제어하는 데 도움이 됩니다. 기본적으로 클리핑 마스크는 레이어의 가시성을 그 레이어 아래의 다른 레이어의 모양으로 제한합니다.

Java에서 클리핑 마스크를 구현하려면 두 개의 레이어가 필요합니다: 기본 레이어와 클리핑할 레이어. 기본 레이어는 가시 유지할 모양 또는 영역을 정의하며, 클리핑할 레이어에는 기본 레이어 모양에 맞이도록 될 내용이 포함되어 있습니다.

Java에서 클리핑 마스크를 적용하면 클리핑된 레이어의 내용은 기본 레이어의 경계 내에서만 가시적입니다. 이러한 경계 바깥의 내용은 숨겨지거나 클리핑됩니다.

클리핑 마스크는 이미지나 아트워크의 특정 영역에 텍스처 또는 패턴과 같은 효과를 적용할 때 특히 유용합니다. 클리핑 마스크를 사용하면 효과를 이미지의 나머지 부분에 영향을 주지 않고 원하는 영역으로 제한할 수 있습니다.

명확한 이해를 위해 페이지 끝의 예제를 참조하십시오.

** 래스터 마스크 ** 

Java 파일의 래스터 마스크는 레이어 내 특정 영역의 가시성을 관리하는 데 사용됩니다. 수학적 모양을 사용하여 마스크된 영역을 정의하는 벡터 마스크와 달리 래스터 마스크는 가시적 또는 숨겨진 영역을 결정하기 위해 픽셀 기반 정보를 활용합니다.

래스터 마스크는 레이어에 적용된 회색조 이미지로 구성됩니다. 마스크의 흰색 영역은 가시성을 나타내며, 검은 색 영역은 숨겨진 부분을 나타냅니다. 사이의 회색 음영은 부분 투명 또는 반투명 영역을 만들 수 있습니다.

더 나은 이해를 위해 페이지 끝의 예제를 참조하십시오.

** 벡터 마스크 **

Java 파일의 벡터 마스크는 레이어 내 특정 영역의 가시성을 수학적 모양을 기반으로 나타내는 다재다능한 도구입니다. 픽셀 기반 데이터에 의존하는 래스터 마스크와 달리 벡터 마스크는 경로와 곡선을 사용하여 부드럽고 크기 조정 가능한 마스크된 영역을 만듭니다.

벡터 마스크는 본질적으로 레이어에 적용된 경로로 구성됩니다. 이 경로의 모양이 레이어의 어떤 부분이 가시적이고 어떤 부분이 숨겨져 있는지 결정합니다. 경로의 제어점과 곡선을 조작하여 정확하고 복잡한 마스크된 영역을 만들 수 있습니다.

벡터 마스크 추가에 대한 자세한 정보는 [벡터 마스크 페이지](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/)를 참조하십시오.

## **예제**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-update-create-layer-mask.java" >}}
