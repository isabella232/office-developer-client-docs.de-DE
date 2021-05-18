---
title: PidTagAdditionalRenEntryIds (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282361"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>PidTagAdditionalRenEntryIds (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-IDs bestimmter Spezieller Ordner. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Kennung:  <br/> |0x36D8  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Die ersten fünf Einträge dieser mehrwertigen Eigenschaft gelten für die folgenden speziellen Ordner, wenn sie im Store vorhanden sind:
  
0 – Konfliktordner
  
1 – Ordner "Synchronisierungsprobleme"
  
2 – Lokaler Fehlerordner
  
3 – Ordner "Serverfehler"
  
4 – Junk-E-Mail-Ordner
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und markiert E-Mail-Nachrichten, die Empfänger dazu verwengen sollen, vertrauliche Informationen (z. B. Kennwörter und andere persönliche Informationen) an eine nicht vertrauenswürdige Quelle zu verschicken.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


[Informationen zur Speicher-API](https://msdn.microsoft.com/library/aa192884.aspx)

