---
title: LISTSEP-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
ms.localizationpriority: medium
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Gibt die Zeichenfolge als Listentrennzeichen für das gebietsschema des aktuellen Benutzers zurück.
ms.openlocfilehash: 5538d8e101ceffe86d33cd4a2e334789203840bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574006"
---
# <a name="listsep-function"></a>LISTSEP Function

Gibt die Zeichenfolge als Listentrennzeichen für das gebietsschema des aktuellen Benutzers zurück.
  
## <a name="syntax"></a>Syntax

LISTSEP ()
  
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="example"></a>Beispiel

SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)") 
  

