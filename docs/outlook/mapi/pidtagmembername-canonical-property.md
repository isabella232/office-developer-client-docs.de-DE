---
title: Kanonische Pidtagmembername (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342483"
---
# <a name="pidtagmembername-canonical-property"></a>Kanonische Pidtagmembername (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Anzeigenamen eines Members der ACL-Tabelle (Access Control List).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W  <br/> |
|Kennung:  <br/> |0x6672  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden von der [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um den Namen eines Members einer ACL-Tabelle anzuzeigen, bei dem es sich um eine Person oder Rolle mit expliziten rechten für einen Ordner oder ein Postfach handelt. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

