---
title: Kanonische Pidtagrulestable (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428501"
---
# <a name="pidtagrulestable-canonical-property"></a>Kanonische Pidtagrulestable (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle mit allen Regeln, die auf einen Ordner angewendet werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULES_TABLE  <br/> |
|Kennung:  <br/> |0x3FE1  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist für alle Folder-Objekte auf einem Exchange-Server vorhanden, die Regeln aufweisen. In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Regeln verwendet. Sie können die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit dem **IID_IExchangeModifyTable** -Schnittstellenbezeichner verwenden, um eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die Rules-Tabelle in einem Ordner abzurufen. Sie können diese Schnittstelle verwenden, um diese Regeln zu lesen und zu ändern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind. 
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

