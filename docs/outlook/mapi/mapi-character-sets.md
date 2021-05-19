---
title: MAPI-Zeichensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417553"
---
# <a name="mapi-character-sets"></a>MAPI-Zeichensätze

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-konforme Clientanwendungen und Dienstanbieter können ANSI-Zeichen (einzelnes Byte) oder Unicode-Zeichen (Doppel-Byte) verwenden. OEM-Zeichensätze werden nicht unterstützt. Eine an eine MAPI-Methode oder -Funktion übergebene OEM-Zeichenfolge verursacht einen Fehler bei dieser Methode oder Funktion. Clientanwendungen, die mit Dateinamen im OEM-Zeichensatz arbeiten, müssen darauf achten, sie in ANSI zu konvertieren, bevor sie an eine MAPI-Methode oder -Funktion übergeben werden.
  
Die Unterstützung des Unicode-Zeichensatz ist optional, sowohl für Clients als auch für Dienstanbieter. Alle Dienstanbieter sollten ihren Code schreiben, damit sie kompilieren können, unabhängig davon, ob sie Unicode unterstützen oder nicht. Clients kompilieren abhängig von ihrer Supportstufe bedingt, Dienstanbieter jedoch nicht. Sie sollten nicht neu kompiliert werden müssen, wenn sich der Zeichensatz ändert. Nichts im Dienstanbietercode sollte bedingt sein. 
  
Wenn Clients oder Dienstanbieter, die Unicode unterstützen, einen Methodenaufruf mit Zeichenzeichenfolgen als Eingabe- oder Ausgabeparameter erstellen, legen sie das MAPI_UNICODE fest. Wenn Sie dieses Flag festlegen, wird für die Implementierung angegeben, dass alle eingehenden Zeichenfolgen Unicode-Zeichenfolgen sind. Bei der Ausgabe fordert das Festlegen dieses Kennzeichens, dass alle von der Implementierung übergebenen Zeichenfolgen möglichst Unicode-Zeichenfolgen sein sollen. Methoden implementierer, die Unicode unterstützen, entsprechen der Anforderung. methoden implementers that do not provide Unicode support will not comply. Zeichenfolgeneigenschaften, die nicht im Unicode-Format vorliegen, sind vom Typ PT_STRING8.
  
MAPI definiert die **fMapiUnicode-Konstante** in der Headerdatei MAPIDEFS. H, um den Standardzeichensatz zu repräsentieren. Wenn ein Client oder Dienstanbieter Unicode unterstützt, **wird fMapiUnicode** auf MAPI_UNICODE. Clients und Dienstanbieter, die Unicode nicht unterstützen, **legen fMapiUnicode auf** Null fest. 
  
Dienstanbieter, die Unicode nicht unterstützen, sollten:
  
- Konvertierungen zwischen Zeichensätzen verweigern.
    
- Übergeben Sie das MAPI_UNICODE in Methodenaufrufen nie.
    
- Gibt MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE übergeben wird.
    
- Deklarieren Sie die Eigenschaften der ANSI-Zeichenfolge explizit. 
    
Dienstanbieter können auch MAPI_E_BAD_CHARWIDTH zurückgeben, wenn sie nur Unicode unterstützen und Clients das MAPI_UNICODE übergeben. 
  
 Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**nur IAddrBook-Implementierung)** 
  
Für diese Methoden können Aufrufer erwarten, dass alle zurückgegebenen Zeichenfolgen Unicode-Zeichenfolgen sind. Zeichenzeichenfolgen, die von MAPI-Implementierungen einer anderen Methode zurückgegeben werden, sind ANSI-Zeichenzeichenfolgen.
  

