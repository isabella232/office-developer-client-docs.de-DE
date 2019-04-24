---
title: Kanonische Pidtaglistunsubscribe (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278879"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Kanonische Pidtaglistunsubscribe (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) Liste-unsubscribe-Kopfzeilenfeld.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Kennung:  <br/> |0x1045  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um ein Listen-unsubscribe-Kopfzeilenfeld zu generieren, müssen Clients diese Eigenschaften auf den gewünschten Wert festlegen. MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld List-unsubscribe kopieren.
  
Um den Wert dieser Listenserver bezogenen Eigenschaften festzulegen, müssen MIME-Clients die in der folgenden Tabelle angegebenen Kopfzeilenfelder schreiben.
  
|**Eigenschaft**|**Bevorzugter Kopfzeilen Feldname**|**Name des alternativen Kopfzeilenfelds**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |Liste-unsubscribe  <br/> |X-List-unsubscribe  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

