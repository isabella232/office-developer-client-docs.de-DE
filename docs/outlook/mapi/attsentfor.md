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
  
Das **attSentFor-Attribut** wird als gezählte Zeichenfolgen codiert, die ende-zu-Ende gelegt werden. Das Format für **attSentFor** lautet wie folgt: 
  
 **attSentFor**: 
  
> display-name-length display-name address-length  _email-address_
    
 _E-Mail-Adresse_
  
> typ **:** address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigenamelänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von nicht signierten langen Ganzzahlen. Sie enthalten jedoch weiterhin das Beenden von Nullzeichen. Der Typ und die Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen literalen Doppelpunkt getrennt (:) zeichen, z. B. "smtp:joe@nowhere.com". Nur der kombinierte Typ **:** adresszeichenfolge ist null-terminated.
  

