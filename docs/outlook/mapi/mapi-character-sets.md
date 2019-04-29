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
  
MAPI-kompatible Clientanwendungen und Dienstanbieter können ANSI-Zeichen (Single Byte) oder Unicode-Zeichen (Double Byte) verwenden. OEM-Zeichensätze werden nicht unterstützt. Eine OEM-Zeichenfolge, die an eine MAPI-Methode oder-Funktion übergeben wird, führt zu einer fehlerhaften Methode oder Funktion. Client Anwendungen, die mit Dateinamen im OEM-Zeichensatz arbeiten, müssen darauf achten, Sie in ANSI zu konvertieren, bevor Sie an eine MAPI-Methode oder-Funktion übergeben werden.
  
Die Unterstützung des Unicode-Zeichensatzes ist optional, sowohl für Clients als auch für Dienstanbieter. Alle Dienstanbieter sollten Ihren Code schreiben, damit er kompiliert werden kann, unabhängig davon, ob er Unicode unterstützt. Clients können abhängig von der jeweiligen Supportstufe bedingt kompiliert werden, jedoch nicht von Dienstanbietern. Sie sollten nicht neu kompiliert werden, wenn sich der Zeichensatz ändert. Nichts in Dienstanbieter Code sollte abhängig sein. 
  
Wenn Clients oder Dienstanbieter, die Unicode unterstützen, einen Methodenaufruf durchführen, der Zeichenfolgen als Eingabe-oder Ausgabeparameter enthält, legen Sie das MAPI_UNICODE-Flag fest. Das Festlegen dieses Flags gibt an, dass alle eingehenden Zeichenfolgen Unicode-Zeichenfolgen sind. Bei der Ausgabe fordert das Festlegen dieses Flags, dass alle Zeichenfolgen, die von der Implementierung zurückgegeben werden, nach Möglichkeit Unicode-Zeichenfolgen sein sollten. Methoden Implementierer, die Unicode unterstützen, erfüllen die Anforderung; Methoden Implementierer, die keine Unicode-Unterstützung bereitstellen, werden nicht erfüllt. Zeichenfolgeneigenschaften, die nicht im Unicode-Format vorliegen, sind vom Typ PT_STRING8.
  
MAPI definiert die **fMapiUnicode** -Konstante in der Headerdatei MAPIDEFS. H zur Darstellung des Standardzeichensatz. Wenn ein Client oder Dienstanbieter Unicode unterstützt, wird **fMapiUnicode** auf MAPI_UNICODE festgelegt. Clients und Dienstanbieter, die den Unicode-Satz **fMapiUnicode** nicht unterstützen. 
  
Dienstanbieter, die Unicode nicht unterstützen, sollten:
  
- Weigern Sie sich, Konvertierungen zwischen Zeichensätzen auszuführen.
    
- Führen Sie das MAPI_UNICODE-Flag nie in Methoden aufrufen weiter.
    
- Gibt MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag übergeben wird.
    
- Deklarieren Sie die ANSI-Zeichenfolgeneigenschaften explizit. 
    
Dienstanbieter können auch MAPI_E_BAD_CHARWIDTH zurückgeben, wenn Sie nur Unicode unterstützen und Clients das MAPI_UNICODE-Flag nicht bestehen. 
  
 Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) (Nur**IAddrBook** -Implementierung) 
  
Für diese Methoden können Aufrufer davon ausgehen, dass zurückgegebene Zeichenfolgen Unicode-Zeichenfolgen sein. Zeichenfolgen, die von MAPI-Implementierungen anderer Methoden zurückgegeben werden, sind ANSI-Zeichenfolgen.
  

