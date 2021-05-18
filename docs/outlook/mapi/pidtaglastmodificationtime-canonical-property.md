---
title: PidTagLastModificationTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279709"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>PidTagLastModificationTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das Datum und die Uhrzeit, zu der das Objekt oder Unterobjekt zuletzt geändert wurde. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Kennung:  <br/> |0x3008  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Nachrichtenzeit  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird zunächst auf denselben Wert wie die **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) festgelegt. Anlagenunterobjekte können sie bei Bedarf aktualisieren, indem sie die letzte Änderungszeit kopieren, die vom systemeigenen Dateisystem verwaltet wird. Eine Clientanwendung kann diese Eigenschaft bis zum ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) festlegen. Von da an sollte der Anbieter die **PR_LAST_MODIFICATION_TIME** bei jedem **IMAPIProp::SaveChanges-Aufruf** aktualisieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
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

