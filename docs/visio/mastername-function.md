---
title: MASTERNAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
ms.localizationpriority: medium
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge "no master" zurück, wenn das Blatt kein Master-Shape besitzt.
ms.openlocfilehash: 209874e1a1c01c607790f5289ab9d8b183c6fc99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612463"
---
# <a name="mastername-function"></a>MASTERNAME Function

Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge " \<no master\> " zurück, wenn das Blatt kein Master-Shape hat.
  
## <a name="syntax"></a>Syntax

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Number** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

