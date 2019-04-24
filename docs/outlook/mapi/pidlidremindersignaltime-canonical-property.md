---
title: Kanonische Pidlidremindersignaltime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350855"
---
# <a name="pidlidremindersignaltime-canonical-property"></a>Kanonische Pidlidremindersignaltime (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Zeitpunkt an, zu dem eine Erinnerung von Ausstehend zu überfällig wechselt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidReminderNextTime  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x00008560  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Erinnerung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss festgelegt werden, wenn die **dispidReminderSet** ([pidlidreminderset (](pidlidreminderset-canonical-property.md))-Eigenschaft true ist. Clients müssen den Wert in koordinierter weltZeit (UTC) festlegen.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

