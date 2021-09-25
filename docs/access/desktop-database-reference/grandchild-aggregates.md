---
title: Enkel-Aggregat
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d55a304c05076a83af25265d51cb0837a7ea1459
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568957"
---
# <a name="grandchild-aggregates"></a>Enkel-Aggregat


**Gilt für**: Access 2013, Office 2013

Die Kapitelspalte, die in einer Klausel eines Shape-Befehls erstellt wurde, erhält möglicherweise einen *Kapitelaliasnamen* (in der Regel mit dem AS-Schlüsselwort). Sie können jede Spalte in jedem Kapitel des formförmigen **Recordsets** mit einem vollqualifizierten Namen identifizieren, der das untergeordnete Element identifiziert, das die Spalte enthält. Wenn z. B. das übergeordnete Kapitel, "chap1", ein untergeordnetes Kapitel enthält, "chap2", das eine Betragsspalte aufweist, dann lautet der qualifizierte Name "chap1.chap2.csv". Der qualifizierte Name kann dann als Argument für eine der Aggregatfunktionen (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY) verwendet werden.

