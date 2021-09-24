---
title: PidTagAttachNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b594a7cd69b6c75b064e30868f3cce0070519246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550834"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zahl, die die Anlage innerhalb der übergeordneten Nachricht eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_NUM  <br/> |
|Kennung:  <br/> |0x0E21  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Nachrichtenspeicher generieren und verwalten diese Eigenschaft. Die Anlagennummer ist der sekundäre Sortierschlüssel nach der Renderingposition in der Anlagentabelle. 
  
 **PR_ATTACH_NUM** wird verwendet, um die Anlage mit der [IMessage::OpenAttach-Methode](imessage-openattach.md) zu öffnen. Innerhalb einer Clientanwendungssitzung bleibt die **PR_ATTACH_NUM** Eigenschaft einer Nachrichtenanlage konstant, solange die Anlagentabelle geöffnet ist. 
  
Der Nachrichtenspeicher gibt Änderungen mithilfe der Methoden **IMessage::CreateAttach** und **IMessage::D eleteAttach** an die Tabelle weiter. Bei dieser Option kann der Nachrichtenspeicher Tabellenbenachrichtigungen für geöffnete Anlagentabellen generieren, sodass Clients diese Änderungen erneut synchronisieren können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

