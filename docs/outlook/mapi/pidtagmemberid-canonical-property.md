---
title: Kanonische Pidtagmemberid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342637"
---
# <a name="pidtagmemberid-canonical-property"></a>Kanonische Pidtagmemberid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Bezeichner eines TABLE-Elements, das über die in einem Microsoft Exchange Server-Ordner oder-Postfach beschriebenen Rechte verfügt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_ID  <br/> |
|Kennung:  <br/> |0x6671  <br/> |
|Datentyp:  <br/> |PT_I8  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt einen eindeutigen Bezeichner für die Tabelle zurück. Jeder Member-ID ist ein Verzeichnis Benutzerbezeichner zugeordnet, der von dieser Eigenschaft angegeben wird. Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um den Verzeichniseintrags Bezeichner eines Members mit expliziten rechten für einen Ordner abzurufen. 
  
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
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagmemberentryid (-Eigenschaft](pidtagmemberentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

