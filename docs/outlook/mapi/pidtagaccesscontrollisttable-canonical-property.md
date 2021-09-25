---
title: PidTagAccessControlListTable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 494a767f08d6ba473ef3260daff5fc122d2926a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563966"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>PidTagAccessControlListTable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle, die aus allen Systemzugriffssteuerungslisten (System Access Control Lists, SACL) besteht, die auf einen Ordner angewendet werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACL_TABLE  <br/> |
|Kennung:  <br/> |0x3FE0  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Zugriffskontrolle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist für alle Ordnerobjekte in einem Exchange Server vorhanden. Die in dieser Eigenschaft enthaltenen Werte werden zum Lesen und Ändern von Zugriffssteuerungslisten (Access Control Lists, ACLs) in Ordnern verwendet. You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder. Sie können diese Schnittstelle verwenden, um diese ACLs zu lesen und zu ändern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

