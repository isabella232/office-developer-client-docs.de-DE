---
title: Kanonische Pidtaglistsubscribe (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279657"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Kanonische Pidtaglistsubscribe (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert des Listen-subscribe-Kopf Felds für MIME-Nachrichten (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Kennung:  <br/> |0x1044  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um ein Listen-subscribe-Kopfzeilenfeld zu generieren, müssen Clients den Wert dieser Eigenschaften auf den gewünschten Wert festlegen. MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld Listen-subscribe kopieren.
  
Um den Wert solcher serverbezogenen Eigenschaften festzulegen, müssen die in der folgenden Tabelle angegebenen Kopfzeilenfelder von MIME-Clients geschrieben werden.
  
|**Eigenschaft**|**Bevorzugter Kopfzeilen Feldname**|**Name des alternativen Kopfzeilenfelds**|
|:-----|:-----|:-----|
|**Pidtaglistsubscribe (** <br/> |Liste abonnieren  <br/> |X-list-subscribe  <br/> |
   
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

