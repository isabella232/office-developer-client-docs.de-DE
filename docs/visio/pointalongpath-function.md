---
title: POINTALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797644"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH Function

Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

POINTALONGPATH (** *Abschnitt* **, ** *Reisen* ** ** *[, Offset]* ** ** *[, Segment]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reisen_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt, der den Punkt bezeichnet. Muss zwischen 0 und 1 liegen.  <br/> |
| _Offset_ <br/> |Optional  <br/> |**Double** <br/> |Der Abstand, um den der Punkt vom Pfad abgesetzt ist. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des Pfads, in dem die Koordinaten berechnet werden sollen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Punkt**
  
## <a name="remarks"></a>Bemerkungen

Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Positive *Offset* -Werte geben Punkten Links der Laufrichtung an. 
  
Negative *Offset* -Werte geben Punkten rechts der Laufrichtung an. 
  
Ein **Point** steht für ein geordnetes Paar geometrischer Koordinaten (*x,y*) als einzelner Wert. 
  

