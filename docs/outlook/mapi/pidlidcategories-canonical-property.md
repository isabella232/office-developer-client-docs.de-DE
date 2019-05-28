---
title: Kanonische pidlidcategories (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344975"
---
# <a name="pidlidcategories-canonical-property"></a>Kanonische pidlidcategories (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine Liste der Kategorien für ein Element an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidCategories  <br/> |
|Eigenschaftengruppe:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Lange ID (LID):  <br/> |0x00002328  <br/> |
|Datentyp:  <br/> |PT_MV_UNICODE  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>Hinweise

Um ein Schlüsselwort-Kopfzeilenfeld zu generieren, müssen Clients den Wert dieser Eigenschaft auf die gewünschten Werte festlegen. Diese Eigenschaft hat mehrere Zeichenfolgen; jede Kategorie sollte einem einzelnen Schlüsselwort zugeordnet werden.
  
MIME-Writer (Multipurpose Internet Mail Extensions) sollten jeden unter Wert dieser Eigenschaft in ein separates Schlüsselwort im Schlüsselwort-Headerfeld kopieren, wobei ein Komma (u + 002C) und ein Leerzeichen (u + 0020) die einzelnen Schlüsselwörter voneinander trennen. MIME-Writer können diese Eigenschaft löschen, anstatt Sie in das Kopfzeilenfeld Schlüsselwörter zu kopieren, um Konflikte zwischen unterschiedlichen Gruppen von Kategorien in unterschiedlichen Organisationen zu vermeiden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt eine Eigenschaftssatzes-Definition und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert aus Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

