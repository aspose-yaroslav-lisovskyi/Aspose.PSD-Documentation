---
title: 既知の問題
type: ドキュメント
weight: 40
url: /ja/net/known-issues/
---

## **.NET Compact Framework**
- 特定のWindowsバージョン（Windows Mobile 5.0-6.0など）では、証明書で署名されたCompact Frameworkアセンブリ（または二重署名された証明書）が期待通りに機能せず、正しくロードされないことが観察されています（TypeLoadExceptionがスローされます）。問題を解決するためには、ユーザーは証明書を削除し、更新されたアセンブリを使用する必要があります。なお、この変更はご自身の責任において行う必要があり、このようなアセンブリの変更により正常に動作することを保証するものではありません。また、潜在的なセキュリティ上の脅威となるため、署名のないアセンブリは出荷していません。代わりに、可能であれば古いオペレーティングシステムの使用を避け、新しいエディションやサービスパックにアップグレードして、証明書の署名に関する問題を解決してください。