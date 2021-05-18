---
title: PidTagStoreEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278750"
---
# <a name="pidtagstoreentryid-canonical-property"></a>PidTagStoreEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den eindeutigen Eintragsbezeichner des Nachrichtenspeichers, in dem sich ein Objekt befindet.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_ENTRYID  <br/> |
|Kennung:  <br/> |0x0FFB  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird verwendet, um einen Nachrichtenspeicher mit der [IMAPISession::OpenMsgStore-Methode zu](imapisession-openmsgstore.md) öffnen. Es wird auch verwendet, um alle Objekte zu öffnen, die im Besitz des Nachrichtenspeichers sind. 
  
Bei einem Nachrichtenspeicher ist diese Eigenschaft mit der eigenen PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) identisch. Eine Clientanwendung kann die beiden Eigenschaften mithilfe der [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) vergleichen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Gibt Postfachordner zwischen Clients zurück.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

