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
description: Gibt den Namen einer Hintergrund als Zeichenfolge zurück.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796528"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME-Funktion

Gibt den Namen einer Hintergrund als Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

BKGPAGENAME (** *LangID_opt* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Numerische** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Hinweise

Wenn die Seite für die Sie die Funktion verwenden ein Hintergrundblatt die Zeichenfolge nicht "\<kein Hintergrund\>" zurückgegeben. 
  
Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

