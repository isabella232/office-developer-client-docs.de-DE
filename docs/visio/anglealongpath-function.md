---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160293"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH Function

Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

ANGLEALONGPATH (***Abschnitt***, ***Reisen*** ***[, Segment]*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
| _segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen _Segment_ Wert einschließen, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück. 
  
Wenn Sie einen _Segment_ Wert einschließen, bestimmt ANGLEALONGPATH den Eckpunkt der Tangente mithilfe von _Reisen_ , um das percertage entlang des _Segments_zu berechnen.
  
Wenn einer der _Abschnitte_ oder _Segmente_ nicht vorhanden ist, gibt Microsoft Visio #Ref! zurück. 
  

