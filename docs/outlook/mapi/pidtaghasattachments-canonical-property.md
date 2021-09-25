---
title: PidTagHasAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95bad8593130ed66868b4b0bffc3c87caf46c1c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563497"
---
# <a name="pidtaghasattachments-canonical-property"></a>PidTagHasAttachments (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn eine Nachricht mindestens eine Anlage enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_HASATTACH  <br/> |
|Kennung:  <br/> |0x0E1B  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichtenspeicher kopiert diese Eigenschaft aus dem **MSGFLAG_HASATTACH** Flag der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft. Eine Clientanwendung kann dann **PR_HASATTACH** verwenden, um nachrichtenanlagen in einer Nachrichtenanzeige zu sortieren. 
  
Der Wert dieser Eigenschaft wird mit der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aktualisiert. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

