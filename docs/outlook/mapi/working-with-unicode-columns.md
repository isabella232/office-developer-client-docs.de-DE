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
ms.openlocfilehash: ffeee38920bf1c864b93e6513913c140cb658d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595307"
---
# <a name="working-with-unicode-columns"></a>Arbeiten mit Unicode-Spalten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeichenfolgen in Tabellen können mit 8-Bit-Zeichen, die Eigenschaftentyp PT_STRING8 sind, oder 16-Bit-Unicode-Zeichen werden Eigenschaftstyp PT_UNICODE dargestellt werden. Tabelle Implementierer können entscheiden, ob ihre Tabellen Unicode-Zeichenfolgen unterstützen. Da Unicode Wert für Clients und -Dienstanbieter hinzugefügt werden durch die Featuregruppe erweitern, wird empfohlen, mit Unicode-Unterstützung, wann immer möglich. 
  
Viele Table-Methoden akzeptieren eine Kennung, die bestimmt, ob Zeichenfolgenwerte-Eigenschaft erwartet Unicode werden oder nicht. Bei der Eingabe gibt an, die Option MAPI_UNICODE angeben der Tabelle Implementierer, dass alle Zeichenfolgenwerte für-Eigenschaft zusammen mit dem Aufruf übergeben Unicode-Zeichenfolgen werden und Eigenschaftentypen von PT_UNICODE haben. Bei der Ausgabe gibt dieses Flag an, dass alle Eigenschaftswerte der zurückgegebenen Zeichenfolge Unicode-Zeichenfolgen, wenn möglich sein soll. Gibt an, ob das Flag für die Eingabe oder Ausgabe eine Bedeutung hat, hängt von der Methode ab. Tabelle Implementierer, die Unicode nicht unterstützt und sind die Option MAPI_UNICODE übergeben zurück den MAPI_E_BAD_CHAR_WIDTH-Wert.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

