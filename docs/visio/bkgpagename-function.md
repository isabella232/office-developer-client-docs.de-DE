---
title: BKGPAGENAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Gibt einen Hintergrundseitennamen als Zeichenfolge zurück.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410315"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME Function

Gibt einen Hintergrundseitennamen als Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional.  <br/> |**Numeric** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Wenn die Seite, für die Sie die Funktion verwenden, keine Hintergrundseite hat, wird die Zeichenfolge \< "kein \> Hintergrund" zurückgegeben. 
  
Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

