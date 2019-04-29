---
title: MSOSHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414494"
---
# <a name="msoshade-function"></a>MSOSHADE Function

Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

MSOSHADE (* * *Color* * *, * * *-deltaLum* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**RGB** <br/> |Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.  <br/> |
| _-deltaLum_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Die prozentuale Änderung in Richtung weiß (-100%) oder schwarz (100%) aus dem _Farbwert_ .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Je näher der _Farbwert_ zu weiß oder schwarz ist, desto kleiner ist die Änderung der Schattierung, die von einem bestimmten _deltaLum-_ Wert erzeugt wird. 
  

