---
title: Kanonische PidLidOfflineStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b0bb4ef47372a3489bfd8050164f1b07fb09178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555692"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Kanonische PidLidOfflineStatus-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidOfflineStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085B9  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Dokument ist nicht ausgecheckt.  <br/> |
|1  <br/> |Das Dokument ist für den aktuellen Benutzer ausgecheckt.  <br/> |
|2  <br/> |Das Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei, die zur Bearbeitung auf dem aktuellen Computer gespeichert wurde.  <br/> |
   
Diese Eigenschaft wird lokal berechnet und zu keinem Zeitpunkt an einen Server gesendet, es sei denn, ein Benutzer zieht das Element auf ein anderes Konto. In diesem Fall wird sie als benutzerdefinierte benutzerdefinierte Eigenschaft behandelt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

