---
title: MSOSHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
ms.openlocfilehash: 76ba30f977b9a08916ba158f474f57dbf2d9a7a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563042"
---
# <a name="msoshade-function"></a>MSOSHADE Function

Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

MSOSHADE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**RGB** <br/> |Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.  <br/> |
| _-deltaLum_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Die prozentuale Änderung in Richtung Weiß (-100 %) oder Schwarz (100 %) vom _Farbwert._  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Je näher der  _Farbwert_ an Weiß oder Schwarz liegt, desto kleiner ist die Änderung des Schattens, der durch einen  _bestimmten DeltaLum-Wert_ erzeugt wird. 
  

