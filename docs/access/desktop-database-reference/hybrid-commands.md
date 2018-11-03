---
title: Hybridbefehle (Access PC-Datenbank-Referenz)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946913"
---
# <a name="hybrid-commands"></a>Hybridbefehle


**Betrifft**: Access 2013, Office 2013

Hybridbefehle sind teilweise parametrisierte Befehle. Beispiel:

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

Das Zwischenspeicherungsverhalten für einen Hybridbefehl unterscheidet sich nicht von dem für reguläre parametrisierte Befehle.

