---
title: Kanonische Pidtagattachnumber (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327251"
---
# <a name="pidtagattachnumber-canonical-property"></a>Kanonische Pidtagattachnumber (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zahl, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_NUM  <br/> |
|Kennung:  <br/> |0x0E21  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher generieren und verwalten diese Eigenschaft. Die Anlagennummer ist der sekundäre Sortierschlüssel nach der Wiedergabeposition in der Anlage Tabelle. 
  
 **PR_ATTACH_NUM** wird zum Öffnen der Anlage mit der [IMessage:: openattach](imessage-openattach.md) -Methode verwendet. Innerhalb einer Client Anwendungssitzung bleibt die **PR_ATTACH_NUM** -Eigenschaft einer Nachrichtenanlage konstant, solange die Anlage Tabelle geöffnet ist. 
  
Der Nachrichtenspeicher propagiert Änderungen an der Tabelle mithilfe der Methoden **IMessage:: createattach** und **IMessage::D eleteattach** . Nach seiner Option kann der nachrichtenspeichertabellen Benachrichtigungen für offene Anlagen Tabellen generieren, sodass Clients erneut eine Synchronisierung mit diesen Änderungen ausführen können. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
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

