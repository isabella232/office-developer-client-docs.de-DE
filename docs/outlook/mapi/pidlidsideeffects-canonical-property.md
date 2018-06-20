---
title: Kanonische PidLidSideEffects-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793784"
---
# <a name="pidlidsideeffects-canonical-property"></a>Kanonische PidLidSideEffects-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Steuert, wie ein Meldungsobjekt vom Client verarbeitet wird, wenn bei der Eingabe der Endbenutzer fungiert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidSideEffects  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008510  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeit-Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Muss auf eine bitweise oder 0 (null) oder mehrere der folgenden Werte festgelegt werden.
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Löschen.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Keine Benutzeroberfläche ist Message-Objekt zugeordnet.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Verschieben oder Kopieren auf ein Folder-Objekt mit einer **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md))-Eigenschaft des "IPF. Hinweis".  <br/> |
|seOpenTocopy  <br/> |0 x 0020  <br/> |Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Kopieren in einen anderen Ordner.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Wechsel zu einem anderen Ordner.  <br/> |
|seOpenForCtxMenu  <br/> |0 x 0100  <br/> |Zusätzliche Verarbeitung muss auf das Objekt "Message" beim Anzeigen von Verben für den Endbenutzer.  <br/> |
|seCannotUndoDelete  <br/> |0 x 0400  <br/> |Löschvorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenToDelete" festgelegt ist.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Kopiervorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenTocopy" festgelegt ist.  <br/> |
|seCannotUndoMove  <br/> |0 x 1000  <br/> |Move-Vorgang kann nicht rückgängig zu machen, müssen nicht festgelegt werden, es sei denn, "SeOpenToMove" festgelegt ist.  <br/> |
|seHasScript  <br/> |0 x 2000  <br/> |Message-Objekts enthält Endbenutzer Skript.  <br/> |
|seOpenToPermDelete  <br/> |0 x 4000  <br/> |Zusätzliche Verarbeitung ist erforderlich, um das Objekt "Message" endgültig löschen.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

