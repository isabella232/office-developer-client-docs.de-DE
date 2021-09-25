---
title: Kanonische PidLidReminderTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f60b025307e26158ffbe5d6bacc0f8a5e29c5fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600540"
---
# <a name="pidlidremindertime-canonical-property"></a>Kanonische PidLidReminderTime-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die anfängliche Signalzeit für eine Erinnerung an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidReminderTime  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008502  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Erinnerung  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Bei Kalenderobjekten stellt diese Eigenschaft die Zeit dar, zu der der Benutzer zu spät kommt, also die Startzeit des Termins. Clients müssen den Wert in koordinierter Weltzeit (COORDINATED Universal Time, UTC) festlegen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für E-Mails und andere Objekterinnerungen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

