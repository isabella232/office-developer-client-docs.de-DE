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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318158"
---
# <a name="attfrom"></a>attFrom

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attFrom** -Attribut wird als **TRP** -Struktur codiert, die den Anzeigenamen und die e-Mail-Adresse des Absenders kodiert, gefolgt von dem Anzeigenamen und der Adresse des Absenders, gefolgt von jedem erforderlichen Abstand. Das Format für **attFrom** lautet wie folgt: 
  
**attFrom**: _TRP-Structure_ Sender-Display-Name _ Absender-Adresse _ Padding 
    
Der Sender-Display-Name ist eine mit NULL endende Zeichenfolge, die bei Bedarf mit einem zusätzlichen NULL-Zeichen aufgefüllt wird, um eine 2-Byte-Grenze zu erreichen. Der Abstand am Ende der **attFrom** -Codierung besteht aus beliebig vielen NULL-Zeichen, um eine **sizeof (TRP)-** Grenze zu erreichen. 
  
_TRP-Struktur:_ **trpidOneOff** cbgrtrp CCH CB 
    
Für das **attFrom** -Element ist die **TRP**-Struktur immer eine einmalige Codierung, sodass die trpid aus dem **TRP**-Structure-Feld immer **trpidOneOff**ist. Die cbgrtrp-, CCH-und CB-Elemente entsprechen den restlichen Feldern der **TRP** -Struktur. 
  
Das cbgrtrp-Feld wird als Summe aus **(sizeof (TRP \*) 2)**, der Länge des null-terminierten Sender-Display-namens mit seinem Abstand und der Länge der null-terminierten Absenderadresse berechnet.
  
Das Feld CCH wird als Länge des mit NULL endenden Anzeige namens mit seinem Abstand berechnet.
  
Das CB-Feld wird als Länge der null-terminierten Absenderadresse berechnet.
  
_Absender-Adresse:_ Address-Type **:** Address **' \ 0 '**
    
Die Absenderadresse ist eine Zeichenfolge, die aus vier Teilen besteht, dem Adresstyp, einem Zeichenfolgenliteral (:), der Adresse selbst und einem abschließenden NULL-Zeichen). Die Zeichenfolge `fax:1-909-555-1234\0` wäre beispielsweise ein gültiger Absender-Adresswert.
  

