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
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424504"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>PidTagAccessControlListTable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle, die aus allen Systemzugriffssteuerungslisten (System Access Control Lists, SACL) besteht, die auf einen Ordner angewendet wurden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACL_TABLE  <br/> |
|Kennung:  <br/> |0x3FE0  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist für alle Ordnerobjekte auf einer Exchange Server. In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Zugriffssteuerungslisten (Access Control Lists, ACLs) in Ordnern verwendet. Sie können die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit der IID_IExchangeModifyTable-Schnittstellen-ID verwenden, um eine [IExchangeModifyTable : IUnknown-Schnittstelle](iexchangemodifytableiunknown.md) zur ACL-Tabelle in einem Ordner zu erhalten.  Sie können diese Schnittstelle verwenden, um diese ACLs zu lesen und zu ändern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

