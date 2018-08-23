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
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588776"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidOfflineStatus  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x000085B9  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Dokument ist nicht ausgecheckt.  <br/> |
|1  <br/> |Dokument wird für den aktuellen Benutzer ausgecheckt.  <br/> |
|2  <br/> |Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei zur Bearbeitung auf dem aktuellen Computer gespeichert.  <br/> |
   
Diese Eigenschaft wird lokal berechnet und wird nicht gesendet auf einen Server können Sie jederzeit, wenn ein Benutzer das Element an ein anderes Konto zieht. In diesem Fall wird es als benutzerdefinierte Eigenschaft benutzerdefinierte behandelt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

