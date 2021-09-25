---
title: PidLidCategories (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 568349edc056db11298668b942130a4e91a8ff3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561131"
---
# <a name="pidlidcategories-canonical-property"></a>PidLidCategories (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine Liste der Kategorien für ein Element an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCategories  <br/> |
|Eigenschaftensatz:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Long ID (LID):  <br/> |0x00002328  <br/> |
|Datentyp:  <br/> |PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um ein Headerfeld für Schlüsselwörter zu generieren, müssen Clients den Wert dieser Eigenschaft auf die gewünschten Werte festlegen. Diese Eigenschaft weist mehrere Zeichenfolgen auf. Jede Kategorie sollte einem einzelnen Schlüsselwort zugeordnet werden.
  
MIME-Autoren (Multipurpose Internet Mail Extensions) sollten jeden Unterwert dieser Eigenschaft in ein separates Schlüsselwort im Kopfzeilenfeld "Schlüsselwörter" kopieren, wobei jedes Schlüsselwort durch Kommas (U+002C) und Leerzeichen (U+0020) getrennt wird. MIME-Autoren können diese Eigenschaft ablegen, anstatt sie in das Kopfzeilenfeld für Schlüsselwörter zu kopieren, um Konflikte zwischen verschiedenen Kategoriengruppen in verschiedenen Organisationen zu vermeiden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Die Definition von Eigenschaftengruppen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

