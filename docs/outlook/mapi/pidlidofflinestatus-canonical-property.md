---
title: Kanonische Pidlidofflinestatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326299"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Kanonische Pidlidofflinestatus (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidOfflineStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x000085B9  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Dokument ist nicht ausgecheckt.  <br/> |
|1  <br/> |Dokument ist für den aktuellen Benutzer ausgecheckt.  <br/> |
|2  <br/> |Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei, die zum Bearbeiten auf dem aktuellen Computer gespeichert wurde.  <br/> |
   
Diese Eigenschaft wird lokal berechnet und wird nicht an einen Server gesendet, es sei denn, ein Benutzer zieht das Element in ein anderes Konto. In diesem Fall wird es als benutzerdefinierte benutzerdefinierte Eigenschaft behandelt.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

