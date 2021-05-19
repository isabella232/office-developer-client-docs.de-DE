---
title: MASTERNAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge "kein Master" zurück, wenn das Blatt keinen Master hat.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414753"
---
# <a name="mastername-function"></a>MASTERNAME Function

Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge "kein Master" zurück, wenn das Blatt keinen \< \> Master hat.
  
## <a name="syntax"></a>Syntax

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional.  <br/> |**Number** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

