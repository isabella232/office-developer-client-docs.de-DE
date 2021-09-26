---
title: BOUNDINGBOXRECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
ms.openlocfilehash: da94210970e1c3331380e1ee319b0ba59230ea68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598717"
---
# <a name="boundingboxrect-function"></a>BOUNDINGBOXRECT Function

Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXRECT(** *Index* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Rand des das Shape umgebenden Felds, für den die Koordinate abgerufen werden soll. Mögliche Werte finden Sie in den Anmerkungen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>HinwBemerkungeneise

 *Index*  kann einer der folgenden Werte sein: 
  
|**Aspekt**|**Wert**|
|:-----|:-----|
|Linker Rand  <br/> |0  <br/> |
|Rechter Rand  <br/> |1  <br/> |
|Oberer Rand  <br/> |2  <br/> |
|Unterer Rand  <br/> |3  <br/> |
   
Wenn das Shape über ein übergeordnetes Shape verfügt, befindet sich der Rückgabewert im Koordinatensystem dieses übergeordneten Elements.
  

