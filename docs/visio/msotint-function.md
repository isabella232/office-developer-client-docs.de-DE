---
title: MSOTINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797563"
---
# <a name="msotint-function"></a>MSOTINT Function

Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

MSOTINT (** *Farbe* **, ** *DeltaLum* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbe_ <br/> |Erforderlich  <br/> |**RGB** <br/> |Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.  <br/> |
| _deltaLum_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Die prozentuale Änderung in Richtung weiß (-100 %) oder Schwarz (100 %) vom Wert _Color_ .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Je näher der _Color_ -Wert ist weiß oder Schwarz ist, desto geringer ist die Änderung am Farbton, die von einem bestimmten _DeltaLum_ -Wert bewirkt wird. 
  

