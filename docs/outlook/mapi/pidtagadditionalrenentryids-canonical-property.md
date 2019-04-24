---
title: Kanonische Pidtagadditionalrenentryids (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282361"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Kanonische Pidtagadditionalrenentryids (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-IDs bestimmter spezieller Ordner. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Kennung:  <br/> |0x36D8  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die ersten fünf Einträge dieser mehrwertigen Eigenschaft gelten für die folgenden speziellen Ordner, wenn Sie im Speicher vorhanden sind:
  
0-Konfliktordner
  
1-Ordner mit Synchronisierungsproblemen
  
Ordner "2-lokale Fehler"
  
Ordner mit 3 Serverfehlern
  
4-Junk-e-Mail-Ordner
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und markiert e-Mail-Nachrichten, die dazu dienen, Empfänger dazu zu verleiten, vertrauliche Informationen (wie Kennwörter und andere persönliche Informationen) an eine nicht vertrauenswürdige Quelle weiterzugeben.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
### <a name="header-files"></a>Header Dateien

Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


[Informationen zur Speicher-API](https://msdn.microsoft.com/library/aa192884.aspx)

