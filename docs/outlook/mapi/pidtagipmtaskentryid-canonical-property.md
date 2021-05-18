---
title: PidTagIpmTaskEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327844"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a>PidTagIpmTaskEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **EntryID** des Ordners Outlook Aufgaben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_TASK_ENTRYID  <br/> |
|Kennung:  <br/> |0x36D4  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird mithilfe des Property- und Stream-Objektprotokolls gelesen oder geschrieben. Sie wird aus dem Posteingang oder Stammordner gelesen und in diesen geschrieben. Die Implementierung muss den Ordner Posteingang verwenden, wenn der Speicher der des primären Messagingbenutzers ist, und sie muss den Stammordner verwenden, wenn der Speicher der eines Stellvertretungsbenutzers ist.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
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

