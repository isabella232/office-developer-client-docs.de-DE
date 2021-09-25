---
title: MSOTINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
ms.openlocfilehash: 6d263872f10971d913938370f580e95fe5d743fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608221"
---
# <a name="msotint-function"></a>MSOTINT Function

Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

MSOTINT(** *color* **, ** *deltaLum* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**RGB** <br/> |Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.  <br/> |
| _deltaLum_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Die prozentuale Änderung in Richtung Weiß (-100 %) oder Schwarz (100 %) vom _Farbwert._  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Je näher der  _Farbwert_ weiß oder schwarz ist, desto kleiner ist die Änderung des Farbtons, der durch einen  _bestimmten DeltaLum-Wert_ erzeugt wird. 
  

