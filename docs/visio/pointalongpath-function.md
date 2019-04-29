---
title: POINTALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430483"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH Function

Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

POINTALONGPATH (* * *section* * *, * * *Reise* * * * * *[, Offset]* * * * * *[, Segment]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt, der den Punkt bezeichnet. Muss zwischen 0 und 1 liegen.  <br/> |
| _Offset_ <br/> |Optional  <br/> |**Double** <br/> |Der Abstand, um den der Punkt vom Pfad abgesetzt ist. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des Pfads, in dem die Koordinaten berechnet werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Point**
  
## <a name="remarks"></a>Bemerkungen

Wenn _section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Positive *Offset* Werte geben Punkte links von der Fahrtrichtung an. 
  
Negative *Offset* Werte geben die Punkte rechts neben der Fahrtrichtung an. 
  
Ein **Point** steht für ein geordnetes Paar geometrischer Koordinaten (*x,y*) als einzelner Wert. 
  

