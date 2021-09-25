---
title: Kanonische PidLidSideEffects-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d8c36f1af61318e7291cfd51166755c8f33c7130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620310"
---
# <a name="pidlidsideeffects-canonical-property"></a>Kanonische PidLidSideEffects-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Steuert, wie ein Nachrichtenobjekt vom Client bei der Verwendung von Endbenutzereingaben behandelt wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSideEffects  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008510  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Muss auf eine bitweise oder null oder mehr der folgenden Flags festgelegt werden.
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Beim Löschen ist eine zusätzliche Verarbeitung für das Nachrichtenobjekt erforderlich.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Dem Nachrichtenobjekt ist keine Benutzeroberfläche zugeordnet.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Beim Verschieben oder Kopieren in ein Ordnerobjekt mit einer **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) -Eigenschaft von "IPF" ist eine zusätzliche Verarbeitung für das Nachrichtenobjekt erforderlich. Hinweis".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Beim Kopieren in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Nachrichtenobjekt erforderlich.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Beim Verschieben in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Nachrichtenobjekt erforderlich.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Beim Anzeigen von Verben für den Endbenutzer ist eine zusätzliche Verarbeitung für das Nachrichtenobjekt erforderlich.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Löschvorgang kann nicht rückgängig gesetzt werden, darf nur festgelegt werden, wenn "seOpenToDelete" festgelegt ist.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Kopiervorgang kann nicht rückgängig macht werden, darf nur festgelegt werden, wenn "seOpenTocopy" festgelegt ist.  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Verschiebungsvorgang kann nicht rückgängig gesetzt werden, es sei denn, "seOpenToMove" ist festgelegt.  <br/> |
|seHasScript  <br/> |0x2000  <br/> |Das Nachrichtenobjekt enthält ein Endbenutzerskript.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Zum dauerhaften Löschen des Nachrichtenobjekts ist eine zusätzliche Verarbeitung erforderlich.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Die Definition von Eigenschaftengruppen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

