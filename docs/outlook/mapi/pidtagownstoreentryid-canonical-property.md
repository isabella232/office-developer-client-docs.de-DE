---
title: Kanonische PidTagOwnStoreEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9ea8af971f9a731aecab0ee6f4b8ea67b651643
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794775"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>Kanonische PidTagOwnStoreEntryId-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Eintrags-ID des Nachrichtenspeichers an einen Transport eng gekoppelten.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|Bezeichner:  <br/> |0x3E06  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenspeicher-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Eintrags-ID für den Informationsspeicher eng gekoppelten, sofern vorhanden. Beispielsweise kann ein Transportdienstes angeben der private Ordner speichern Eintrags-ID, damit die MAPI-Warteschlange in der Adressbuchhierarchie im Speicher eine Verbindung herstellen kann.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

