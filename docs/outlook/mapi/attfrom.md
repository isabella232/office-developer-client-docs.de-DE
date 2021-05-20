---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432415"
---
# <a name="attfrom"></a>attFrom

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attFrom-Attribut** wird als **TRP-Struktur** codiert, die den Anzeigenamen und die E-Mail-Adresse des Absenders codiert, gefolgt vom Anzeigenamen und der Adresse des Absenders, gefolgt von einem erforderlichen Abstand. Das Format für **attFrom** lautet wie folgt: 
  
**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding 
    
Der Sender-display-name ist eine null-beendete Zeichenfolge, die bei Bedarf mit einem zusätzlichen Nullzeichen gepolstert wird, um eine 2-Byte-Grenze zu erreichen. Der Abstand am Ende der **attFrom-Codierung** besteht aus so vielen Nullzeichen wie nötig, um eine **Sizeof(TRP)-Grenze zu** erreichen. 
  
_TRP-struktur:_ **trpidOneOff** cbgrtrp cch cb 
    
Für das **attFrom-Element** ist die **TRP-Struktur** immer eine einmalige Codierung, daher ist der Trpid aus dem **TRP**-structure-Feld **immer trpidOneOff**. Die cbgrtrp-, cch- und cb-Elemente entsprechen den verbleibenden Feldern der **TRP-Struktur.** 
  
Das cbgrtrp-Feld wird als Summe **von (sizeof(TRP) \* 2),** der Länge des null-terminated sender-display-name mit dem Abstand und der Länge der null-terminated sender-address berechnet.
  
Das #A0 wird als Länge des mit Null beendeten Anzeigenamens mit seinem Abstand berechnet.
  
Das cb-Feld wird als Länge der mit Null beendeten Absenderadresse berechnet.
  
_sender-address:_ address-type **:** address **'\0'**
    
Die Absenderadresse ist eine Zeichenfolge, die aus vier Teilen besteht, dem Adresstyp, einem literalen Doppelpunkt (:), der Adresse selbst und einem endenden Nullzeichen. Die Zeichenfolge wäre z. `fax:1-909-555-1234\0` B. ein gesetzlicher Absenderadressenwert.
  

