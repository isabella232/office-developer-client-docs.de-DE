---
title: PidTagMemberEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794600"
---
# <a name="pidtagmemberentryid-canonical-property"></a>PidTagMemberEntryId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält den Directory Eintrag Objektbezeichner des Mitglied Tabelle System Access Control List (SACL).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Bezeichner:  <br/> |0x0FFF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird durch die [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um eine Person oder Rolle, denen die SACL gilt, eindeutig zu identifizieren. Nachdem ein Element in der SACL-Tabelle erstellt wurde, kann die **ENTRYID** geändert werden. Zum Ändern dieser Einstellung müssen Sie das Tabelle Element löschen und mit einem anderen **ENTRYID**neu erstellen.
  
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

