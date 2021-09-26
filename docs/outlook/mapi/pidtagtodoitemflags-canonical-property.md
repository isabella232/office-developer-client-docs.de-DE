---
title: PidTagToDoItemFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dff7b95c0fe95b4f06eae8bf787ee5e8170bff71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629697"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>PidTagToDoItemFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die gekennzeichnete Bedingung eines To-Do Elements dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Kennung:  <br/> |0x0E2B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden soll, wenn die zugehörige Bedingung in der folgenden Tabelle zutrifft, andernfalls 0.
  
||||
|:-----|:-----|:-----|
|Numerischer Wert  <br/> |Name  <br/> |Beschreibung  <br/> |
|Nicht vorhanden  <br/> |Nicht zutreffend  <br/> |Nicht entflaggt  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objekt ist Zeit gekennzeichnet  <br/> |
|8   <br/> |todoRecipientFlagged  <br/> |Sollte nur für ein Nachrichtenentwurfsobjekt festgelegt werden, was bedeutet, dass das Objekt für Empfänger gekennzeichnet ist.  <br/> |
   
Alle Bits, die nicht in der Tabelle angegeben sind, sind reserviert. Sie müssen ignoriert werden, sollten jedoch beibehalten werden, wenn sie festgelegt sind.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

