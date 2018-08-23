---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578038"
---
# <a name="attowner"></a>attOwner

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gezählte Zeichenfolgen End-to-End-festgelegten, wird das Attribut **AttOwner** codiert. Das Format für **AttOwner** lautet wie folgt: 
  
 **AttOwner**: 
  
> Display Name Länge Anzeigename Adresse Länge- _e-Mail-Adresse_
    
 _e-Mail-Adresse_
  
> Adresse vom Typ **:** 
    
Im Gegensatz zu anderen Länge sind Werte, die Anzeige-Namen- und Adresse Länge 16-Bit-Werte ohne Vorzeichen, anstatt lange ganze Zahlen ohne Vorzeichen. Dazu gehören weiterhin Null-Zeichen jedoch beendet. Die Typ und die Adresse Zeichenfolgen in den Eintrag _e-Mail-Adresse_ werden durch einen Doppelpunkt (:)) Literalzeichen wie "smtp:joe@nowhere.com" getrennt. Nur die kombinierten Typ **:** Adresszeichenfolge ist Null endende.
  
Die Zuordnung der MAPI-Eigenschaften in das Attribut **AttOwner** ist abhängig von der Nachrichtenklasse der Nachricht codiert. 
  

