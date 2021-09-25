---
title: PAGENAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
ms.localizationpriority: medium
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Gibt den Seitennamen als Zeichenfolge zurück.
ms.openlocfilehash: 6c9db7a5820a543f4dbe26d27094f858606917e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623285"
---
# <a name="pagename-function"></a>PAGENAME Function

Gibt den Seitennamen als Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

PAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Number** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.
  

