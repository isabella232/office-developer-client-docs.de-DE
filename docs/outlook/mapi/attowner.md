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
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427654"
---
# <a name="attowner"></a>attOwner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attOwner** -Attribut wird als gezählte Zeichenfolge mit End-to-End-Codierung codiert. Das Format für **attOwner** lautet wie folgt: 
  
 **attOwner**: 
  
> Anzeigename-length-Anzeigename-Adresslänge- _e-Mail-Adresse_
    
 _e-Mail-Adresse_
  
> Typ **:** Address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigename-length und die Address-length nicht signierte lange ganze Zahlen, 16-Bit-Werte ohne Vorzeichen. Sie enthalten jedoch weiterhin NULL-Zeichen. Die Typ-und Adress Zeichenfolgen im _e-Mail-Adress_ Eintrag werden durch einen Literalwert (:) Zeichen, wie "SMTP:Joe@nowhere.com". Nur der kombinierte Typ **:** Address String is null-terminated.
  
Die Zuordnung von MAPI-Eigenschaften zum **attOwner** -Attribut hängt von der Nachrichtenklasse der zu codierenden Nachricht ab. 
  

