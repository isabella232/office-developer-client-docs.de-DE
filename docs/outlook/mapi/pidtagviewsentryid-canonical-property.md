---
title: PidTagViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795280"
---
# <a name="pidtagviewsentryid-canonical-property"></a>PidTagViewsEntryId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Die Eintrags-ID des Ordners benutzerdefinierte Ansichten enthält.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Bezeichner:  <br/> |0x35E5  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der gemeinsamen Ordner anzeigen enthält ein vordefiniertes Satzes von Standardansicht Bezeichner, während der Ansichtordner Bezeichner definiert durch ein messaging-Benutzer enthält. Diese Ordner, die nicht in der Hierarchie zwischen Personen Nachricht (IPM) sichtbar sind, können enthalten viele Ansicht Bezeichner, die jeweils als eine Nachricht gespeichert. Die Client-Anwendung kann wahlweise Zusammenführen von zwei Sätze der Bezeichner und diese beiden zur Verfügung stellen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

