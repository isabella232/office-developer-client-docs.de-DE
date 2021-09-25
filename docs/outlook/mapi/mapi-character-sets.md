---
title: MAPI-Zeichensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a98a9731f9d08f5a223a34faaaa4e14756559ef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556203"
---
# <a name="mapi-character-sets"></a>MAPI-Zeichensätze

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-kompatible Clientanwendungen und Dienstanbieter können ANSI-Zeichen (einzelnes Byte) oder Unicode-Zeichen (Doppelbyte) verwenden. OEM-Zeichensätze werden nicht unterstützt. Eine OEM-Zeichenfolge, die an eine MAPI-Methode oder -Funktion übergeben wird, führt dazu, dass diese Methode oder Funktion fehlschlägt. Clientanwendungen, die mit Dateinamen im OEM-Zeichensatz arbeiten, müssen sorgfältig in ANSI konvertiert werden, bevor sie an eine MAPI-Methode oder -Funktion übergeben werden.
  
Die Unterstützung des Unicode-Zeichensatzes ist optional, sowohl für Clients als auch für Dienstanbieter. Alle Dienstanbieter sollten ihren Code schreiben, damit sie kompilieren können, unabhängig davon, ob sie Unicode unterstützen oder nicht. Clients kompilieren bedingt, abhängig von ihrem Supportgrad, Dienstanbieter jedoch nicht. Sie sollten nicht neu kompiliert werden müssen, wenn sich der Zeichensatz ändert. Im Dienstanbietercode sollte nichts bedingt sein. 
  
Wenn Clients oder Dienstanbieter, die Unicode unterstützen, einen Methodenaufruf ausführen, der Zeichenfolgen als Eingabe- oder Ausgabeparameter enthält, legen sie das MAPI_UNICODE Flag fest. Das Festlegen dieses Flags gibt der Implementierung an, dass alle eingehenden Zeichenfolgen Unicode-Zeichenfolgen sind. Bei der Ausgabe fordert das Festlegen dieses Flags an, dass alle von der Implementierung zurückgegebenen Zeichenfolgen nach Möglichkeit Unicode-Zeichenfolgen sein sollen. Methoden implementer that support Unicode will comply with the request; Methoden implementer that do not provide Unicode support will not comply. Zeichenfolgeneigenschaften, die nicht im Unicode-Format vorliegen, sind vom Typ PT_STRING8.
  
MAPI definiert die **fMapiUnicode** -Konstante in der Headerdatei MAPIDEFS. H, um den Standardzeichensatz darzustellen. Wenn ein Client oder Dienstanbieter Unicode unterstützt, wird **fMapiUnicode** auf MAPI_UNICODE festgelegt. Clients und Dienstanbieter, die Unicode nicht unterstützen, legen **fMapiUnicode** auf Null fest. 
  
Dienstanbieter, die Unicode nicht unterstützen, sollten Folgendes tun:
  
- Durchführen von Konvertierungen zwischen Zeichensätzen wird abgelehnt.
    
- Übergeben Sie niemals das MAPI_UNICODE Flag in Methodenaufrufen.
    
- Gibt MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag übergeben wird.
    
- Deklarieren Sie ANSI-Zeichenfolgeneigenschaften explizit. 
    
Dienstanbieter können auch MAPI_E_BAD_CHARWIDTH zurückgeben, wenn sie nur Unicode unterstützen und Clients das flag MAPI_UNICODE nicht übergeben. 
  
 Die aktuelle Version der MAPI unterstützt Unicode in den folgenden Methoden: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**Nur IAddrBook-Implementierung)** 
  
Für diese Methoden können Aufrufer davon ausgehen, dass es sich bei allen zurückgegebenen Zeichenfolgen um Unicode-Zeichenfolgen handelt. Zeichenzeichenfolgen, die von MAPI-Implementierungen einer anderen Methode zurückgegeben werden, sind ANSI-Zeichenzeichenfolgen.
  

