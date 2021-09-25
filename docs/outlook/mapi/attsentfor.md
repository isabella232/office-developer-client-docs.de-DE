---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e78fe61824984ab61a9b12fcc4866bc91848be79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605146"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **Attribut "attSentFor"** wird als gezählte Zeichenfolgen codiert, die end-to-end angeordnet sind. Das Format für **attSentFor** lautet wie folgt: 
  
 **attSentFor:** 
  
> _E-Mail-Adresse_ der Länge des Anzeigenamens
    
 _E-Mail-Adresse_
  
> type **:** address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigenamenlänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von unsignierten langen ganzzahligen Zahlen. Sie enthalten jedoch weiterhin Nullzeichen. Die Typ- und Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen Literalkolon (:) zeichen, z. B. "smtp:joe@nowhere.com". Nur der kombinierte Typ **:** Die Adresszeichenfolge wird mit NULL beendet.
  

