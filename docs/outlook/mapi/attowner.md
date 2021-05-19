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
  
Das **attOwner-Attribut** wird als gezählte Zeichenfolgen codiert, die ende-zu-Ende gelegt werden. Das Format für **attOwner** lautet wie folgt: 
  
 **attOwner**: 
  
> display-name-length display-name address-length  _email-address_
    
 _E-Mail-Adresse_
  
> typ **:** address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigenamelänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von nicht signierten langen Ganzzahlen. Sie enthalten jedoch weiterhin das Beenden von Nullzeichen. Der Typ und die Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen literalen Doppelpunkt getrennt (:) zeichen, z. B. "smtp:joe@nowhere.com". Nur der kombinierte Typ **:** adresszeichenfolge ist null-terminated.
  
Die Zuordnung von MAPI-Eigenschaften zum **attOwner-Attribut** hängt von der Nachrichtenklasse der zu codierten Nachricht ab. 
  

