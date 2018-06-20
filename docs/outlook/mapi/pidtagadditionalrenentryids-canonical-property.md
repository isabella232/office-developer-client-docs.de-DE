---
title: Kanonische PidTagAdditionalRenEntryIds-Eigenschaft
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
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794045"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Kanonische PidTagAdditionalRenEntryIds-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Eintrags-IDs für bestimmte Spezialordner. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Bezeichner:  <br/> |0x36D8  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Die ersten fünf Einträge in diesem mehrwertigen Eigenschaft gelten folgenden Spezialordner, sofern sie im Speicher vorhanden sind:
  
0 – Konfliktordner
  
1 – Sync-Probleme-Ordner
  
2 - Ordner Lokale Fehler
  
3 - Ordner Server-Fehler
  
4 - junk-e-Mail-Ordner
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifiziert und e-Mail-Nachrichten, die an Empfänger Preisgabe von vertraulichen Informationen (wie Kennwörter und andere persönliche Informationen) zu einer nicht vertrauenswürdigen Quelle markiert.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


[Über den API-Speicher](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

