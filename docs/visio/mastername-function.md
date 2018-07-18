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
description: Gibt den Namen eines Zeichenblatts Master-Shape als Zeichenfolge zurück, oder gibt die Zeichenfolge "kein Master-Shape" zurück, wenn das Blatt nicht über ein Master-Shape verfügt.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797456"
---
# <a name="mastername-function"></a>MASTERNAME Function

Gibt den Namen eines Zeichenblatts Master-Shape als Zeichenfolge zurück oder die Zeichenfolge "\<kein Master-Shape\>" Wenn das Blatt nicht über ein Master-Shape verfügt.
  
## <a name="syntax"></a>Syntax

MASTERNAME ([** *LangID_opt* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Nummer** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

