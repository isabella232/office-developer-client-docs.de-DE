---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341419"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH Function

Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

ANGLEALONGPATH (* * *section* * *, * * *Reise* * * * * *[, Segment]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen _Segment_ Wert angeben, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück. 
  
Wenn Sie einen _Segment_ Wert angeben, bestimmt ANGLEALONGPATH den Punkt der Tangente, indem Sie die Option _Reisen_ zum Berechnen der percertage im _Segment_verwenden.
  
Wenn ein _Abschnitt_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

