---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3b149b3b9a28cdf4043ace5da667b18729a077d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572102"
---
# <a name="attfrom"></a>attFrom

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attFrom-Attribut** wird als **TRP-Struktur** codiert, die den Anzeigenamen und die E-Mail-Adresse des Absenders codiert, gefolgt vom Anzeigenamen und der Adresse des Absenders, gefolgt von einem erforderlichen Abstand. Das Format für **attFrom** lautet wie folgt: 
  
**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding 
    
Der Absenderanzeigename ist eine Zeichenfolge, die mit null terminiert ist und ggf. mit einem zusätzlichen NULL-Zeichen versehen ist, um eine 2-Byte-Grenze zu erreichen. Der Abstand am Ende der **attFrom-Codierung** besteht aus so vielen Nullzeichen wie erforderlich, um eine **Sizeof(TRP)-Grenze** zu erreichen. 
  
_TRP-struktur:_ **trpidOneOff** cbgrtrp cch cb 
    
Für das **attFrom-Element** ist die **TRP-Struktur** immer eine einmalige Codierung, sodass der Trpid aus dem **TRP-Strukturfeld** immer **trpidOneOff** ist. Die Cbgrtrp-, CCH- und CB-Elemente entsprechen den verbleibenden Feldern der **TRP-Struktur.** 
  
Das cbgrtrp-Feld wird als Summe von **(sizeof(TRP) \* 2)** berechnet, der Länge des absenderanzeigennamens mit Null-Termin mit seinem Abstand und der Länge der Absenderadresse, die mit NULL beendet wurde.
  
Das CCH-Feld wird als Die Länge des mit Null beendeten Anzeigenamens mit seinem Abstand berechnet.
  
Das CB-Feld wird als Die Länge der Absenderadresse berechnet, die mit NULL beendet wurde.
  
_sender-address:_ address-type **:** address **'\0'**
    
Die Absenderadresse ist eine Zeichenfolge, die aus vier Teilen besteht, dem Adresstyp, einem Literalkolon (:), der Adresse selbst und einem endenden NULL-Zeichen. Die Zeichenfolge wäre beispielsweise `fax:1-909-555-1234\0` ein zulässiger Absenderadressenwert.
  

