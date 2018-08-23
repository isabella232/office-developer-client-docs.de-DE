---
title: PidTagSwappedToDoData (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8086bc3ea35fdbb4e0f7758b7931e305259a3a9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578668"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verwaltet einen zweiten Satz von Eigenschaftswerten, die keine Auswirkung auf die gekennzeichneten Zustand des Message-Objekts.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Kennung:  <br/> |0x0E2D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Als den Speicherort des sekundären Flag fungiert, wenn Flags Absender oder Absender Erinnerungen unterstützt werden, enthält diese Struktur einen Speicherort zum Speichern aller Eigenschaften sich auf das Informationszwecken kennzeichnen Protokoll beziehen, die in den Absender Flags unterstützt werden, und alle Eigenschaften für das Reminder-Einstellungen-Protokoll, die in Absender Erinnerungen unterstützt werden, ohne das Flag Absender oder Absender Erinnerungsinformationen an die Empfänger einer Nachricht verfügbar zu machen.
  
In ähnlicher Weise stellt diese Struktur einen Speicherort zum Speichern aller die Eigenschaften für das Informationszwecken Protokoll kennzeichnen, die in den Empfänger Flags unterstützt werden und Eigenschaften für das Protokoll der Erinnerung Einstellungen, die im Empfänger unterstützt werden Erinnerungen für eine zuvor gesendete Nachricht.
  
Weitere Informationen zu dieser Eigenschaft finden Sie unter [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.
    
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

