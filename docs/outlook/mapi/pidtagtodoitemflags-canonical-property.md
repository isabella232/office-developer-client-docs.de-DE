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
ms.openlocfilehash: 79f6c90d1ebd2257cc428e88dfce3d9ee9dfeccf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573467"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>PidTagToDoItemFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Stellt ein Aufgabenelement gekennzeichnete Bedingung dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Kennung:  <br/> |0x0E2B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden sollte, wenn die zugeordnete Bedingung in der folgenden Tabelle angewendet wird, sonst 0.
  
||||
|:-----|:-----|:-----|
|Numerischen Wert  <br/> |Name  <br/> |Beschreibung  <br/> |
|Nicht vorhanden  <br/> |–  <br/> |Nicht gekennzeichnet  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objekt ist Zeit gekennzeichnet  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Sollte nur auf einem Objekt "Message" Entwurf festgelegt werden, und das bedeutet, dass das Objekt für die Empfänger gekennzeichnet ist.  <br/> |
   
Alle Bits an, die nicht in der Tabelle angegeben wurden, sind reserviert. Sie müssen ignoriert werden, aber Sie erhalten bleiben sollen, wenn sie festgelegt sind.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

