---
title: Enkel-Aggregat
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292146"
---
# <a name="grandchild-aggregates"></a>Enkel-Aggregat


**Gilt für**: Access 2013, Office 2013

Die Chapter-Spalte, die in einer Klausel eines Shape-Befehls erstellt wurde, kann einen *Kapitel-Aliasnamen* erhalten (normalerweise mit dem As-Schlüsselwort). Sie können jede Spalte in einem beliebigen Kapitel des geformten **Recordset-Objekts** mit einem vollqualifizierten Namen identifizieren, der das untergeordnete Element der Spalte identifiziert. Wenn beispielsweise das übergeordnete Chapter, chap1, ein untergeordnetes Chapter (chap2) enthält, das eine Betragsspalte "Amt" aufweist, lautet der qualifizierte Name chap1. chap2. Amt. Der qualifizierte Name kann dann als Argument für eine der Aggregatfunktionen verwendet werden (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY).

