---
title: PidLidOfflineStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418834"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidOfflineStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x000085B9  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Das Dokument ist nicht ausgecheckt.  <br/> |
|1  <br/> |Das Dokument wird für den aktuellen Benutzer ausgecheckt.  <br/> |
|2  <br/> |Das Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei, die für die Bearbeitung auf dem aktuellen Computer gespeichert ist.  <br/> |
   
Diese Eigenschaft wird lokal berechnet und zu keinem Zeitpunkt an einen Server gesendet, es sei denn, ein Benutzer zieht das Element in ein anderes Konto. In diesem Fall wird sie als benutzerdefinierte benutzerdefinierte Eigenschaft behandelt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

