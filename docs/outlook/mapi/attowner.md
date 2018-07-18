---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791342"
---
# <a name="attowner"></a>attOwner

  
  
**Betrifft**: Outlook 
  
Gezählte Zeichenfolgen End-to-End-festgelegten, wird das Attribut **AttOwner** codiert. Das Format für **AttOwner** lautet wie folgt: 
  
 **AttOwner**: 
  
> Display Name Länge Anzeigename Adresse Länge- _e-Mail-Adresse_
    
 _e-Mail-Adresse_
  
> Adresse vom Typ **:** 
    
Im Gegensatz zu anderen Länge sind Werte, die Anzeige-Namen- und Adresse Länge 16-Bit-Werte ohne Vorzeichen, anstatt lange ganze Zahlen ohne Vorzeichen. Dazu gehören weiterhin Null-Zeichen jedoch beendet. Die Typ und die Adresse Zeichenfolgen in den Eintrag _e-Mail-Adresse_ werden durch einen Doppelpunkt (:)) Literalzeichen wie "smtp:joe@nowhere.com" getrennt. Nur die kombinierten Typ **:** Adresszeichenfolge ist Null endende.
  
Die Zuordnung der MAPI-Eigenschaften in das Attribut **AttOwner** ist abhängig von der Nachrichtenklasse der Nachricht codiert. 
  

