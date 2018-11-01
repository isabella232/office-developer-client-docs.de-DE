---
title: Untergeordnete Aggregate
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c5ab45412b0524bcef14a952f5c5bbe0953278c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873530"
---
# <a name="grandchild-aggregates"></a>Grandchild Aggregates


**Betrifft**: Access 2013, Office 2013

Die in einer Klausel eines Strukturierungsbefehls erstellte Kapitelspalte erhält möglicherweise einen Kapitelaliasnamen (üblicherweise mit dem Schlüsselwort AS). Sie können eine Spalte in einem beliebigen Kapitel des strukturierten Recordset-Objekts mit einem vollqualifizierten Namen bezeichnen, durch den das untergeordnete Recordset identifiziert wird, das die Spalte enthält. Wenn z. B. das übergeordnete Kapitel, Kapitel1, ein untergeordnetes Kapitel, Kapitel2 enthält, das eine Mengenspalte, Menge, enthält, würde der qualifizierte Name Kapitel1.Kapitel2.Menge lauten. Der qualifizierte Name kann dann als Argument in einer der Aggregatfunktionen (SUM, AVG, MAX, MIN, COUNT, STDEV oder ANY) verwendet werden.

