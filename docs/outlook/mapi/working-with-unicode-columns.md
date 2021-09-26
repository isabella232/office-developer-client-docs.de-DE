---
title: Arbeiten mit Unicode-Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 762d8acf3ad006380611025fcfce7675c4a3f0bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629431"
---
# <a name="working-with-unicode-columns"></a>Arbeiten mit Unicode-Spalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeichenzeichenfolgen in Tabellen können mit standardmäßigen 8-Bit-Zeichen dargestellt werden, bei denen es sich um Eigenschaftentyp PT_STRING8 handelt, oder mit 16-Bit-Unicode-Zeichen, die Eigenschaftstyp PT_UNICODE sind. Tabellen implementierer können frei auswählen, ob ihre Tabellen Unicode-Zeichenfolgen unterstützen. Da Unicode einen Mehrwert für Clients und Dienstanbieter bietet, indem der Featuresatz erweitert wird, wird empfohlen, Unicode nach Möglichkeit zu unterstützen. 
  
Viele Tabellenmethoden akzeptieren ein Kennzeichen, das bestimmt, ob Zeichenfolgeneigenschaftswerte Unicode sein sollen. Bei der Eingabe gibt das MAPI_UNICODE Flag an, dass alle mit dem Aufruf übergebenen Zeichenfolgeneigenschaftswerte Unicode-Zeichenfolgen und Eigenschaftstypen von PT_UNICODE sind. Bei der Ausgabe gibt dieses Kennzeichen an, dass alle zurückgegebenen Zeichenfolgeneigenschaftswerte nach Möglichkeit Unicode-Zeichenfolgen sein sollen. Ob das Flag eine Bedeutung für die Eingabe oder Ausgabe hat, hängt von der Methode ab. Tabellen implementer that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

