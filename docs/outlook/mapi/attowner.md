---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9f0254b275ea0245360eba39c249139e7b33288
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572109"
---
# <a name="attowner"></a>attOwner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attOwner-Attribut** wird als gezählte Zeichenfolgen codiert, die end-to-end angeordnet sind. Das Format für **attOwner** lautet wie folgt: 
  
 **attOwner**: 
  
> _E-Mail-Adresse_ der Länge des Anzeigenamens
    
 _E-Mail-Adresse_
  
> type **:** address 
    
Im Gegensatz zu anderen Längenwerten sind die Anzeigenamenlänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von unsignierten langen ganzzahligen Zahlen. Sie enthalten jedoch weiterhin Nullzeichen. Die Typ- und Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen Literalkolon (:) zeichen, z. B. "smtp:joe@nowhere.com". Nur der kombinierte Typ **:** Die Adresszeichenfolge wird mit NULL beendet.
  
Die Zuordnung von MAPI-Eigenschaften zum **attOwner-Attribut** hängt von der Nachrichtenklasse der zu codierten Nachricht ab. 
  

