---
title: Kanonische Pidtagmemberentryid (-Eigenschaft
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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342497"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Kanonische Pidtagmemberentryid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner des Verzeichnisobjekts für ein SACL-Tabellenelement (System Access Control List).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Kennung:  <br/> |0X0fff dar  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um eine Person oder Rolle, für die die SACL gilt, eindeutig zu identifizieren. Nachdem ein Element in der SACL-Tabelle erstellt wurde, **** kann es nicht mehr geändert werden. Um Sie zu ändern, müssen Sie das Table-Element löschen und es mit einer anderen **Eintrags**-Nr. neu erstellen.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

