---
title: Dazwischenliegende Shape COMPUTE-Klauseln
TOCTitle: Intervening Shape COMPUTE clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: baed73952acd45e8dba9662191a4d0dfb6bdddad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577262"
---
# <a name="intervening-shape-compute-clauses"></a>Dazwischenliegende Shape COMPUTE-Klauseln


**Gilt für**: Access 2013, Office 2013

Mindestens eine COMPUTE-Klausel kann, wie im folgenden Beispiel dargestellt, zwischen dem übergeordneten und untergeordneten Element in einem parametrisierten SHAPE-Befehl eingefügt werden:

```vb 
 
SHAPE {select au_lname, state from authors} APPEND 
 ((SHAPE 
 (SHAPE 
 {select * from authors where state = ?} rs 
 COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
 BY au_id) rs2 
 COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0) 
```

