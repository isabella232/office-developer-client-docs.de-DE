---
title: Kanonische PidTagAccessControlListTable-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d992c7ac43c736e01184e1f12b3ad366587c9b06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794021"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Kanonische PidTagAccessControlListTable-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Tabelle, die alle System Access Control Lists (SACL) in einen Ordner angewendet besteht.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ACL_TABLE  <br/> |
|Bezeichner:  <br/> |0x3FE0  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Steuerung des Zugriffs  <br/> |
   
## <a name="remarks"></a>Hinweise

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

