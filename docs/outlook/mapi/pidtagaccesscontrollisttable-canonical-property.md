---
title: PidTagAccessControlListTable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 40a2bc8a27ec3ce3df610b9c7364719c2b5ee750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572788"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>PidTagAccessControlListTable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle, die alle System Access Control Lists (SACL) in einen Ordner angewendet besteht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACL_TABLE  <br/> |
|Kennung:  <br/> |0x3FE0  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Steuerung des Zugriffs  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist für alle Ordnerobjekte, die auf einem Exchange-Server vorhanden. Werte enthalten, die in dieser Eigenschaft wird zum Lesen und ändern die Steuerung des Zugriffs Zugriffssteuerungslisten (ACLs) für Ordner. Sie können die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der **IID_IExchangeModifyTable** Interface Identifier verwenden, erhalten eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die ACL-Tabelle in einem Ordner. Sie können diese Schnittstelle zum Lesen und Ändern von ACLs verwenden. 
  
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

