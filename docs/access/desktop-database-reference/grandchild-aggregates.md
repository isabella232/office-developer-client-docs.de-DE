---
title: Untergeordnete Aggregate
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947938"
---
# <a name="grandchild-aggregates"></a>Untergeordnete Aggregate


**Betrifft**: Access 2013, Office 2013

Die in einer Klausel eines Strukturierungsbefehls erstellte Kapitelspalte erhält möglicherweise einen Kapitelaliasnamen (üblicherweise mit dem Schlüsselwort AS). Sie können eine Spalte in einem beliebigen Kapitel des strukturierten Recordset-Objekts mit einem vollqualifizierten Namen bezeichnen, durch den das untergeordnete Recordset identifiziert wird, das die Spalte enthält. Wenn z. B. das übergeordnete Kapitel, Kapitel1, ein untergeordnetes Kapitel, Kapitel2 enthält, das eine Mengenspalte, Menge, enthält, würde der qualifizierte Name Kapitel1.Kapitel2.Menge lauten. Der qualifizierte Name kann dann als Argument in einer der Aggregatfunktionen (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY) verwendet werden.

