---
title: PidLidSideEffects (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331297"
---
# <a name="pidlidsideeffects-canonical-property"></a>PidLidSideEffects (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Steuert, wie ein Nachrichtenobjekt vom Client behandelt wird, wenn es auf Endbenutzereingaben angewendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSideEffects  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008510  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Muss auf einen bitweisen oder null oder mehr der folgenden Flags festgelegt werden.
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Beim Löschen ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Dem Message-Objekt ist keine Benutzeroberfläche zugeordnet.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Beim Verschieben oder Kopieren in ein Folder-Objekt mit einer **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md))-Eigenschaft von "IPF" ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich. Hinweis".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Beim Kopieren in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Beim Verschieben in einen anderen Ordner ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Beim Anzeigen von Verben für den Endbenutzer ist eine zusätzliche Verarbeitung für das Message-Objekt erforderlich.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Löschvorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenToDelete" festgelegt ist.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Kopiervorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenTocopy" festgelegt ist.  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Vorgang kann nicht rückgängig gemacht werden, darf nur festgelegt werden, wenn "seOpenToMove" festgelegt ist.  <br/> |
|seHasScript  <br/> |0x2000  <br/> |Das Message-Objekt enthält ein Endbenutzerskript.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Zusätzliche Verarbeitung ist erforderlich, um das Nachrichtenobjekt dauerhaft zu löschen.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

