---
title: Arbeiten mit Unicodespalten
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
# <a name="working-with-unicode-columns"></a>Arbeiten mit Unicodespalten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeichenzeichenfolgen in Tabellen können mit standardmäßigen 8-Bit-Zeichen dargestellt werden, bei denen es sich um Eigenschaftentyp PT_STRING8 oder 16-Bit-Unicode-Zeichen handelt, bei denen es sich um Eigenschaftstyptypen PT_UNICODE. Tabellen implementierer können auswählen, ob ihre Tabellen Unicode-Zeichenfolgen unterstützen. Da Unicode sowohl für Clients als auch für Dienstanbieter einen Mehrwert bietet, wird die Unterstützung von Unicode nach Möglichkeit empfohlen. 
  
Viele Tabellenmethoden akzeptieren ein Flag, das bestimmt, ob Zeichenfolgeneigenschaftswerte Unicode sein sollen. Bei der Eingabe gibt das Angeben des MAPI_UNICODE-Flag an den Tabellen implementier an, dass alle mit dem Aufruf übergebenen Zeichenfolgeneigenschaftswerte Unicode-Zeichenfolgen sind und Eigenschaftentypen von PT_UNICODE. Bei der Ausgabe gibt dieses Flag an, dass alle zurückgegebenen Zeichenfolgeneigenschaftswerte nach Möglichkeit Unicode-Zeichenfolgen sein sollten. Ob das Flag eine Bedeutung für die Eingabe oder Ausgabe hat, hängt von der Methode ab. Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

