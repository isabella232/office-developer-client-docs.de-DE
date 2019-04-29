---
title: Arbeiten mit Unicode-Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408383"
---
# <a name="working-with-unicode-columns"></a>Arbeiten mit Unicode-Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeichenfolgen in Tabellen können mit standardmäßigen 8-Bit-Zeichen, die Eigenschaftentyp PT_STRING8, oder 16-Bit-Unicode-Zeichen, die Eigenschaftentyp PT_UNICODE sind, dargestellt werden. Tabellen Implementierer können wählen, ob Ihre Tabellen Unicode-Zeichenfolgen unterstützen. Da Unicode für Clients und Dienstanbieter einen Wert hinzufügt, indem der Featuresatz erweitert wird, wird empfohlen, Unicode möglichst zu unterstützen. 
  
Viele Table-Methoden akzeptieren ein Flag, das angibt, ob Zeichenfolgen-Eigenschaftswerte als Unicode erwartet werden. Bei der Eingabe gibt das MAPI_UNICODE-Flag der Tabellen Implementierung an, dass alle mit dem Aufruf übergebenen Zeichenfolgen-Eigenschaftswerte Unicode-Zeichenfolgen und Eigenschaftentypen von PT_UNICODE aufweisen. Bei der Ausgabe gibt dieses Flag an, dass alle zurückgegebenen Zeichenfolgen Eigenschaftswerte nach Möglichkeit Unicode-Zeichenfolgen sein sollten. Ob die Kennzeichnung eine Bedeutung für Eingabe oder Ausgabe hat, hängt von der Methode ab. Tabellen Implementierer, die Unicode nicht unterstützen und übergeben werden das MAPI_UNICODE-Flag gibt den MAPI_E_BAD_CHAR_WIDTH-Wert zurück.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

