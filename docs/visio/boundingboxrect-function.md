---
title: BOUNDINGBOXRECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418071"
---
# <a name="boundingboxrect-function"></a>BOUNDINGBOXRECT Function

Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXRECT (* * *Index* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Rand des das Shape umgebenden Felds, für den die Koordinate abgerufen werden soll. Mögliche Werte finden Sie in den Anmerkungen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>Bemerkungen

 *Index* kann einer der folgenden Werte sein. 
  
|**Item**|**Wert**|
|:-----|:-----|
|Linker Rand  <br/> |0  <br/> |
|Rechter Rand  <br/> |1  <br/> |
|Oberer Rand  <br/> |2  <br/> |
|Unterer Rand  <br/> |3  <br/> |
   
Wenn die Form über ein übergeordnetes Shape verfügt, ist der Rückgabewert im Koordinatensystem des übergeordneten Elements.
  

