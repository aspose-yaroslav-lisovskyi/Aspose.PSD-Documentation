---
title: Aspose.PSD for Python でマスクを使用する方法
weight: 100
type: docs
description: PSDファイル内のクリッピング、ラスター、ベクトルマスクの動作方法の例
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, python, code sample]
url: ja/python-net/update-create-layer-mask/
---

## **概要**

**概要**

PSDファイルには3種類のマスクがあります：
1. クリッピングマスク
2. ラスターマスク
3. ベクトルマスク

この記事では、これら3つのタイプについて説明します。

**クリッピングマスク**

クリッピングマスクは、グラフィックデザインや画像編集ソフトウェアで強力な機能です。これにより、1つのレイヤーの表示を、別のレイヤーの形状や内容に基づいて制御できます。つまり、クリッピングマスクは、下にある他のレイヤーの形状にレイヤーの表示を制限します。

クリッピングマスクを作成するには、まず2つのレイヤーが必要です：ベースレイヤーとクリッピングしたいレイヤーです。ベースレイヤーが表示される形状や領域を定義し、クリッピングしたいレイヤーがベースレイヤーの形状にクリッピングされるコンテンツを含みます。

クリッピングマスクを適用すると、クリッピングされたレイヤーのコンテンツは、ベースレイヤーの境界内でのみ表示されます。ベースレイヤーの境界外のコンテンツは非表示またはクリッピングされます。

クリッピングマスクは、画像や作品の特定領域にテクスチャやパターンなどの効果を適用したい場合に特に便利です。クリッピングマスクを使用することで、画像の他の部分に影響を与えることなく、効果を希望する領域に制限できます。

ページの最後にある例をご確認ください

**ラスターマスク**

PSDファイルのラスターマスクは、レイヤー内の特定の領域の表示を制御するために使用されます。マスクされた領域を定義するために数学的な形状を使用するベクトルマスクとは異なり、ラスターマスクはピクセルベースの情報を使用してどの部分が表示され、隠されるかを決定します。

ラスターマスクは、レイヤーに適用されるグレースケール画像で構成されています。マスクの白色領域は表示される部分を示し、黒色領域は非表示部分を示します。灰色の濃淡は、部分的な透明性やセミ表示領域を作成するために使用できます。

ページの最後にある例をご確認ください

**ベクトルマスク**

PSDファイルのベクトルマスクは、数学的形状に基づいてレイヤー内の特定領域の表示を定義するために使用される多目的なツールです。ピクセルベースの情報を使用するラスターマスクとは異なり、ベクトルマスクはパスと曲線を使用してスムーズかつスケーラブルなマスク領域を作成します。

ベクトルマスクは、基本的にレイヤーに適用されるパスです。パスの形状は、レイヤーのどの部分が表示され、どの部分が非表示になるかを決定します。パスの制御点と曲線を操作することで、正確で複雑なマスク領域を作成できます。

ベクトルマスクの追加方法については、[ベクトルマスクページ](psd/ja/net/layer-vector-mask/)をご覧ください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-update-create-layer-mask.py" >}}