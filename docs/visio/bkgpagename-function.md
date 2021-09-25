---
title: BKGPAGENAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
ms.localizationpriority: medium
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Gibt einen Namen der Hintergrundseite als Zeichenfolge zurück.
ms.openlocfilehash: 96e475690fafee2aba534419578428ad96320e3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554845"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME Function

Gibt einen Namen der Hintergrundseite als Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Seite, für die Sie die Funktion verwenden, keine Hintergrundseite hat, wird die Zeichenfolge " \<no background\> " zurückgegeben. 
  
Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

