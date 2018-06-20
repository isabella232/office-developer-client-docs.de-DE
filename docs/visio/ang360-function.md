---
title: ANG360-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Ein Winkel normalisiert.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796390"
---
# <a name="ang360-function"></a>ANG360 Function

Normalisiert eines Winkels 0 \<Ergebnis = \< 2PI Bogenmaß (0 \<Ergebnis = \< 360-Grad).
  
## <a name="syntax"></a>Syntax

ANG360 (** *Winkel* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Der zu normalisierende Winkel.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Winkel* mithilfe von Winkel Einheiten nicht angegeben ist, wird er als Bogenmaß (Radiant) interpretiert. Wenn *Winkel* auf einen Wert, der ein #VALUE konvertiert werden kann. Fehler wird zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

ANG360(395 deg)
  
Gibt 35 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ANG360(-9,8 rad.)
  
Gibt 2,7664 Rad zurück.
  
## <a name="example-3"></a>Beispiel 3

ANG360(45)
  
Gibt 58,31 deg (1,0177 Rad) zurück.
  

