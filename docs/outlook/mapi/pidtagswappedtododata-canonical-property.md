---
title: PidTagSwappedToDoData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b63e12eb69aff565d3d4ef99b66a5ad364b7cc08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578935"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Behält einen zweiten Satz von Eigenschaftswerten bei, die sich nicht auf den gekennzeichneten Status des Message-Objekts auswirken.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Kennung:  <br/> |0x0E2D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Struktur fungiert als speicherort für sekundäre Flags, wenn Absenderkennzeichen oder Absendererinnerungen unterstützt werden, und stellt einen Speicherort bereit, an dem alle Eigenschaften im Zusammenhang mit dem Informational Flagging-Protokoll gespeichert werden, die in Absenderkennzeichen unterstützt werden, sowie alle Eigenschaften im Zusammenhang mit dem Reminder Einstellungen Protocol, die in Absendererinnerungen unterstützt werden, ohne den Empfängern einer Nachricht die Absenderkennzeichen oder Absendererinnerungsinformationen zur Verfügung zu stellen.
  
Ebenso stellt diese Struktur einen Speicherort bereit, an dem alle Eigenschaften im Zusammenhang mit dem Informational Flagging Protocol gespeichert werden, die in Empfängerflags und Eigenschaften im Zusammenhang mit dem Reminder Einstellungen Protocol unterstützt werden, die in Empfängererinnerungen in einer zuvor gesendeten Nachricht unterstützt werden.
  
Weitere Informationen zu dieser Eigenschaft finden Sie unter [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für E-Mails und andere Objekterinnerungen an.
    
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

