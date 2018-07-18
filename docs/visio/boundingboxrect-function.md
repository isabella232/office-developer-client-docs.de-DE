---
title: BOUNDINGBOXRECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796551"
---
# <a name="boundingboxrect-function"></a>BOUNDINGBOXRECT Function

Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXRECT (** *Index* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Rand des das Shape umgebenden Felds, für den die Koordinate abgerufen werden soll. Mögliche Werte finden Sie in den Anmerkungen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Nummer**
  
## <a name="remarks"></a>Bemerkungen

 *Index* kann eine der folgenden Werte sein: 
  
|**Element**|**Wert**|
|:-----|:-----|
|Linker Rand  <br/> |0  <br/> |
|Rechter Rand  <br/> |1  <br/> |
|Oberer Rand  <br/> |2  <br/> |
|Unterer Rand  <br/> |3  <br/> |
   
Wenn die Form ein übergeordnetes Objekt ist, ist der Rückgabewert im Koordinatensystem des übergeordneten.
  

