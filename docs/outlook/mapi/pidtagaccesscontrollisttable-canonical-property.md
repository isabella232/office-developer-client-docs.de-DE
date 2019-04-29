---
title: Kanonische Pidtagaccesscontrollisttable (-Eigenschaft
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
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Kanonische Pidtagaccesscontrollisttable (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle, die aus allen SACL-Systemen (System Access Control Lists) besteht, die auf einen Ordner angewendet werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACL_TABLE  <br/> |
|Kennung:  <br/> |0x3FE0  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist für alle Folder-Objekte auf einem Exchange-Server vorhanden. In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Zugriffssteuerungslisten (Access Control Lists, ACLs) für Ordner verwendet. Sie können die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit dem **IID_IExchangeModifyTable** -Schnittstellenbezeichner verwenden, um eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die ACL-Tabelle in einem Ordner abzurufen. Sie können diese Schnittstelle verwenden, um diese ACLs zu lesen und zu ändern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

