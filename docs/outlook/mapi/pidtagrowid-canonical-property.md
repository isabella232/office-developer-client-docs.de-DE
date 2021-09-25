---
title: Kanonische PidTagRowid-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21faf4891e1cf827fa575b54de831c7a88f22a29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591500"
---
# <a name="pidtagrowid-canonical-property"></a>Kanonische PidTagRowid-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen Bezeichner für einen Empfänger in einer Empfängertabelle oder Statustabelle.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROWID  <br/> |
|Kennung:  <br/> |0x3000  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |ALLGEMEINE MAPI  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist ein temporärer Wert, der nur für die Lebensdauer des Objekts gültig ist, das die Tabelle besitzt. Sie wird als Spalte der Tabelle angezeigt, aber nicht gespeichert.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

