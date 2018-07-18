---
title: MAPI-Zeichensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f94823eb3f90ff9ac0f472a2de64e1904920d9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792960"
---
# <a name="mapi-character-sets"></a>MAPI-Zeichensätze

  
  
**Betrifft**: Outlook 
  
MAPI-kompatible Clientanwendungen und Dienstanbieter können ANSI-Zeichen (Einzelbyte) oder Unicode-Zeichen (Doppelbyte) verwenden. OEM-Zeichensätze werden nicht unterstützt. OEM-Zeichenfolge an eine MAPI-Methode übergeben, oder Funktion bewirkt, dass diese Methode oder die Funktion ein Fehler auftritt. Clientanwendungen, die Dateinamen in der OEM-Zeichensatz entwickelt dürfen in ANSI umwandeln, bevor sie ein MAPI-Methode oder die Funktion übergeben werden.
  
Mit der Unicode-Unterstützung ist Zeichensatz optional, sowohl für Clients und -Dienstanbieter. Alle-Dienstanbieter sollte ihr Code geschrieben werden, damit sie kompilieren können, unabhängig davon, ob sie Unicode unterstützen. Clients bedingt, je nach ihrer Ebene der Unterstützung von kompilieren, Dienstanbieter jedoch nicht. Sie sollten keine erneut kompiliert werden, wenn der Zeichensatz geändert wird. Nichts Service Provider Code sollte bedingte sein. 
  
Bei Festlegung Clients oder Dienstanbieter, die Unicode-stellen einen Methodenaufruf unterstützen, der Zeichenfolgen als ein-oder Ausgabeparameter enthält sie die Option MAPI_UNICODE. Wenn Sie dieses Flag die Implementierung zeigt an, dass alle eingehende Zeichenfolgen Unicode-Zeichenfolgen werden. Bei der Ausgabe sollte das Festlegen dieses Flag-Anforderungen, die alle Zeichenfolgen übergeben von der Implementierung zu sichern sein Unicode-Zeichenfolgen wenn möglich. Methode Implementierer, die Unicode unterstützen, werden die Anforderung entsprechen. Methode Implementierer, die keine Unicode-Unterstützung bieten werden nicht entsprechen. String-Eigenschaften, die nicht im Unicode-Format sind, sind vom Typ PT_STRING8.
  
MAPI definiert die **fMapiUnicode** -Konstante in der Headerdatei MAPIDEFS. H, um den Standardzeichensatz darstellen. Wenn ein Client oder Dienstanbieter Unicode unterstützt, wird auf Parameter MAPI_UNICODE **fMapiUnicode** festgelegt. **FMapiUnicode** festlegen auf NULL, Clients und Dienstanbieter, die Unicode nicht unterstützen. 
  
Dienstanbieter, die Unicode nicht unterstützen soll:
  
- Zum Durchführen von Konvertierungen zwischen Zeichensätzen ablehnen.
    
- Übergeben Sie die Option MAPI_UNICODE nie-Methode aufrufen.
    
- MAPI_E_BAD_CHARWIDTH zurück, wenn die Option MAPI_UNICODE übergeben wird.
    
- Deklarieren Sie ANSI-Zeichenfolgeneigenschaften explizit. 
    
Dienstanbieter können auch zurückgeben MAPI_E_BAD_CHARWIDTH, wenn sie nur Unicode- und -Clients unterstützen die Option MAPI_UNICODE nicht übergeben. 
  
 Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Nur**IAddrBook** -Implementierung) 
  
Für diese Methoden können Anrufer zurückgegebenen Zeichenfolgen Unicode-Zeichenfolgen zu erwarten. Von MAPI-Implementierungen von einer anderen Methode zurückgegebene Zeichenfolgen werden ANSI-Zeichenfolgen.
  

