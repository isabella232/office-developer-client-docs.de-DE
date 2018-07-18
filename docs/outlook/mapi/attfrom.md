---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791348"
---
# <a name="attfrom"></a>attFrom

**Betrifft**: Outlook 
  
Das Attribut **AttFrom** ist als **TRP** Struktur codiert, die den Anzeigenamen und die e-Mail-Adresse des Absenders, gefolgt vom Anzeigenamen und die Adresse des Absenders, gefolgt von erforderlichen Abstände codiert. Das Format für **AttFrom** lautet wie folgt: 
  
**AttFrom**: _TRP-Struktur_ Absender Anzeigenamen _ Absenderadresse _ Textabstand 
    
Die Absender-Anzeigename ist eine Null endende Zeichenfolge, die Sie bei Bedarf eine 2-Byte-Grenze erreichen mit einem zusätzlichen Null-Zeichen aufgefüllt wird. Der Abstand am Ende der **AttFrom** Codierung besteht aus beliebig viele Null Zeichen Bedarf eine Grenze **sizeof(TRP)** zu erreichen. 
  
_TRP-Struktur:_ **TrpidOneOff** Cbgrtrp Cch cb 
    
Für das Element der **TRP** **AttFrom** -Struktur ist immer ein einmaligen Codierung, also die Trpid deaktiviert die **TRP**-Strukturfeld wird immer **TrpidOneOff**. Die Cbgrtrp, Cch und Cb-Elementen entsprechen die verbleibenden Felder der Struktur **TRP** . 
  
Das Feld Cbgrtrp wird als Summe der berechnet **(sizeof(TRP) \*2)**, die Länge Null endende Absender-Anzeige-Namen seiner Abstand und die Länge Null endende-die Adresse des Absenders.
  
Das Feld Cch wird als die Länge des Null endende-Anzeigenamens mit den Textabstand berechnet.
  
Das Cb-Feld ist als die Länge der Absenderadresse Null endende berechnet.
  
_-Absenderadresse:_ Adresstyp **:** beheben **'\0'**
    
Die Adresse des Absenders ist eine Zeichenfolge, die aus vier Teilen, den Adresstyp, ein literal Doppelpunkt (:)), die Adresse selbst und Endzeichen Null ist. Beispielsweise die Zeichenfolge `fax:1-909-555-1234\0` wäre ein rechtliche Absenderadresse-Wert.
  

