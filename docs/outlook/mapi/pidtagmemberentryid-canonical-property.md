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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433038"
---
# <a name="pidtagmemberentryid-canonical-property"></a>PidTagMemberEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Verzeichnisobjekteintrags-ID eines Sacl-Tabellenmitglieds (System Access Control List).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Kennung:  <br/> |0x0FFF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von der [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) verwendet, um eine Person oder Rolle eindeutig zu identifizieren, auf die die SACL angewendet wird. Nachdem ein Element in der SACL-Tabelle erstellt wurde, kann **die ENTRYID** nicht geändert werden. Um es zu ändern, müssen Sie das Tabellenmitglied löschen und es mit einer anderen **ENTRYID neu erstellen.**
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

