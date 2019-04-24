---
title: Kanonische Pidtagswappedtododata (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359136"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Kanonische Pidtagswappedtododata (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet einen zweiten Satz von Eigenschaftswerten, die sich nicht auf den gekennzeichneten Status des Message-Objekts auswirken.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Kennung:  <br/> |0x0E2D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Als sekundäres Flag-Speicherplatz fungieren wenn Absender Kennzeichen oder Absender Erinnerungen unterstützt werden, bietet diese Struktur einen Speicherort, an dem alle Eigenschaften im Zusammenhang mit dem Informations Protokoll, das in Absender-Flags unterstützt wird, gespeichert werden, und alle Eigenschaften im Zusammenhang mit dem Protokoll für Erinnerungseinstellungen, die in Absender Erinnerungen unterstützt werden, ohne die Absender Kennzeichnung oder Absender Erinnerungsinformationen an die Empfänger einer Nachricht zu übertragen.
  
Entsprechend bietet diese Struktur einen Speicherort für alle Eigenschaften im Zusammenhang mit dem Informations Protokoll, die in Empfänger Kennzeichen und Eigenschaften in Bezug auf das Protokoll für Erinnerungseinstellungen unterstützt werden, das im Empfänger unterstützt wird. Erinnerungen für eine zuvor gesendete Nachricht.
  
Weitere Informationen zu dieser Eigenschaft finden Sie unter [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.
    
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

