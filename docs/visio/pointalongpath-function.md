---
title: POINTALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
ms.openlocfilehash: b436378ee874c3ecf3fc51d07ac80f461c6cfa3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598423"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH Function

Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt, der den Punkt bezeichnet. Muss zwischen 0 und 1 liegen.  <br/> |
| _Offset_ <br/> |Optional  <br/> |**Double** <br/> |Der Abstand, um den der Punkt vom Pfad abgesetzt ist. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
| _segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des Pfads, in dem die Koordinaten berechnet werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Point**
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn _kein Abschnitt_ oder _Segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Positive  *Offsetwerte*  geben Punkte links von der Bewegungsrichtung an. 
  
Negative  *Offsetwerte*  geben Punkte rechts von der Bewegungsrichtung an. 
  
Ein **Point** steht für ein geordnetes Paar geometrischer Koordinaten (*x,y*) als einzelner Wert. 
  

