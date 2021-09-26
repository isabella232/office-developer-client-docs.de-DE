---
title: NAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
ms.localizationpriority: medium
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Gibt den Namen eines Blatts als Zeichenfolge zurück.
ms.openlocfilehash: 7b3bf74d87c534dc99c4ca74d014ded676d0190f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627898"
---
# <a name="name-function"></a>NAME Function

Gibt den Namen eines Blatts als Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

NAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Number** <br/> |Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet. 
  

