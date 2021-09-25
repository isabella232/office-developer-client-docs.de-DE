---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: c7b82a32820de6a0f1faacc8dcf990edb202ca84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578249"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH Function

Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

ANGLEALONGPATH(***Section**_, _*_travel_*_ _*_ [,segment]_** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
| _segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie einen  _Segmentwert_ einschließen, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück. 
  
Wenn Sie einen  _Segmentwert_ einschließen, bestimmt ANGLEALONGPATH den Punkt des Tangens, indem die  _Reise_ verwendet wird, um das Zertifikat entlang des  _Abschnitts_ zu berechnen.
  
Wenn kein _Abschnitt_ oder _Segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

