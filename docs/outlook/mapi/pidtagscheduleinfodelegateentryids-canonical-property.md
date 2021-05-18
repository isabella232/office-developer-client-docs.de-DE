---
title: PidTagScheduleInfoDelegateEntryIds (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321294"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a>PidTagScheduleInfoDelegateEntryIds (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **EntryIDs** der Delegaten. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_DELEGATE_ENTRYIDS  <br/> |
|Kennung:  <br/> |0x6845  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Hinweise

Jeder Eintrag muss den Wert der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft des Adressbucheintrags jeder Stellvertretung enthalten. Diese Eigenschaft muss im Stellvertretungsinformationsobjekt festgelegt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
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

