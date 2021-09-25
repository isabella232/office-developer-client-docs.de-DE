---
title: Hybridbefehle (Access-Desktopdatenbankreferenz)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7c7768ab15659abcf1ab49cb03524f4871616740
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552828"
---
# <a name="hybrid-commands"></a>Hybridbefehle


**Gilt für**: Access 2013, Office 2013

Hybridbefehle sind teilweise parametrisierte Befehle. Beispiel:

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

Das Zwischenspeicherungsverhalten für einen Hybridbefehl unterscheidet sich nicht von dem für reguläre parametrisierte Befehle.

