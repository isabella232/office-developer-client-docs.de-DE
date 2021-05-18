---
title: PidLidReminderOverride (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4956ce33d00135c34193dec3df832c6878b2c6db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360108"
---
# <a name="pidlidreminderoverride-canonical-property"></a>PidLidReminderOverride (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob der Client die Werte der **Eigenschaften dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) und **dispidReminderFileParam** ( [ PidLidReminderFileParameter](pidlidreminderfileparameter-canonical-property.md)) respektieren soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidReminderOverride  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x0000851C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Erinnerung  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Client kann Standardwerte statt der Werte der **Eigenschaften dispidReminderPlaySound** und **dispidReminderFileParam** verwenden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

