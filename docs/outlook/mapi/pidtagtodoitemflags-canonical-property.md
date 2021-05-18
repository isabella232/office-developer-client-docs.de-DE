---
title: PidTagToDoItemFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284483"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>PidTagToDoItemFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Represents a To-Do item's flagged condition.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Kennung:  <br/> |0x0E2B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden sollte, wenn die zugeordnete Bedingung in der folgenden Tabelle zutrifft, andernfalls 0.
  
||||
|:-----|:-----|:-----|
|Numerischer Wert  <br/> |Name  <br/> |Beschreibung  <br/> |
|Nicht vorhanden  <br/> |Nicht zutreffend  <br/> |Unflagged  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objekt ist zeitflagt  <br/> |
|8   <br/> |todoRecipientFlagged  <br/> |Sollte nur für ein Nachrichtenentwurfsobjekt festgelegt werden, was bedeutet, dass das Objekt für Empfänger gekennzeichnet ist.  <br/> |
   
Alle Bits, die nicht in der Tabelle angegeben sind, sind reserviert. Sie müssen ignoriert werden, sollten jedoch beibehalten werden, wenn sie festgelegt sind.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

