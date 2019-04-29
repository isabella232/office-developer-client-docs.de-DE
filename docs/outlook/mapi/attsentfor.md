---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408838"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attSentFor** -Attribut wird als gezählte Zeichenfolge mit End-to-End-Codierung codiert. Das Format für **attSentFor** lautet wie folgt: 
  
 **attSentFor**: 
  
> Anzeigename-length-Anzeigename-Adresslänge- _e-Mail-Adresse_
    
 _e-Mail-Adresse_
  
> Typ **:** Address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigename-length und die Address-length nicht signierte lange ganze Zahlen, 16-Bit-Werte ohne Vorzeichen. Sie enthalten jedoch weiterhin NULL-Zeichen. Die Typ-und Adress Zeichenfolgen im _e-Mail-Adress_ Eintrag werden durch einen Literalwert (:) Zeichen, wie "SMTP:Joe@nowhere.com". Nur der kombinierte Typ **:** Address String is null-terminated.
  

