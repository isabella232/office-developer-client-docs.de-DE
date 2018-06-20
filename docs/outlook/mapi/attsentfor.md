---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791362"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Betrifft**: Outlook 
  
Gezählte Zeichenfolgen End-to-End-festgelegten, wird das Attribut **AttSentFor** codiert. Das Format für **AttSentFor** lautet wie folgt: 
  
 **AttSentFor**: 
  
> Display Name Länge Anzeigename Adresse Länge- _e-Mail-Adresse_
    
 _e-Mail-Adresse_
  
> Adresse vom Typ **:** 
    
Im Gegensatz zu anderen Länge sind Werte, die Anzeige-Namen- und Adresse Länge 16-Bit-Werte ohne Vorzeichen, anstatt lange ganze Zahlen ohne Vorzeichen. Dazu gehören weiterhin Null-Zeichen jedoch beendet. Die Typ und die Adresse Zeichenfolgen in den Eintrag _e-Mail-Adresse_ werden durch einen Doppelpunkt (:)) Literalzeichen wie "smtp:joe@nowhere.com" getrennt. Nur die kombinierten Typ **:** Adresszeichenfolge ist Null endende.
  

