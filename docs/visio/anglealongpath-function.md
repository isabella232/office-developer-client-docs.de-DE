---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796420"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH-Funktion

Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010 
  
## <a name="syntax"></a>Syntax

ANGLEALONGPATH (** *Abschnitt* **, ** *Reisen* ** ** *[, Segment]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reisen_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Wert für _Segment_ eingeschlossen, gibt ANGLEALONGPATH den Wert für dieses Segment nur zurück. 
  
Wenn Sie einen Wert für _Segment_ eingeschlossen, bestimmt ANGLEALONGPATH den Punkt der Tangente mithilfe von _unterwegs sind_ , um den Prozentsatz entlang _Segment_zu berechnen.
  
Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

