---
title: PidTagAttachNumber (kanonische Eigenschaft)
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
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794111"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Zahl, die die Anlage innerhalb der übergeordneten Nachricht eindeutig identifiziert. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_NUM  <br/> |
|Bezeichner:  <br/> |0x0E21  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher generieren und verwalten diese Eigenschaft. Die Anzahl der Anlage ist die sekundäre Sortierschlüssel, nach dem Renderingposition in der Anlagentabelle. 
  
 **PR_ATTACH_NUM** wird zum Öffnen der Anlage mit der [IMessage::OpenAttach](imessage-openattach.md) -Methode verwendet. Innerhalb einer Clientanwendung-Sitzung bleibt die **PR_ATTACH_NUM** -Eigenschaft des e-Mail-Anlagen konstant, wie die Anlagentabelle geöffnet ist. 
  
Der Nachrichtenspeicher verteilt die Änderungen auf die Tabelle mit den Methoden **IMessage::CreateAttach** und **IMessage::DeleteAttach** . Ermessen kann der Nachrichtenspeicher Tabelle Benachrichtigungen auf Anlage öffnen Tabellen generieren, damit Clients auf diese Änderungen synchronisieren können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

