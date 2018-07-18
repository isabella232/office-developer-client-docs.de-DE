---
title: PidTagResourceMethods (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794965"
---
# <a name="pidtagresourcemethods-canonical-property"></a>PidTagResourceMethods (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske der Flags, die die Methoden in der Schnittstelle **IMAPIStatus** angeben, die durch die Statusobjekt unterstützt werden. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Bezeichner:  <br/> |0x3E02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, welche der Methoden in der Implementierung der **IMAPIStatus** ein Statusobjekt unterstützt werden. Status-Objekte sind zulässig, nicht unterstützten Methoden MAPI_E_NO_SUPPORT zurückgegeben. 
  
Clients verwenden ein Statusobjekt **PR_RESOURCE_METHODS** -Eigenschaft, um das Aufrufen von nicht unterstützten Methoden zu vermeiden. Wenn das Flag, das eine bestimmte Methode entspricht, festgelegt ist, wird die Methode vorhanden ist und aufgerufen werden kann. Wenn Flags deaktiviert ist, sollte die Methode nicht aufgerufen werden. 
  
Die Status-Objekte, die von MAPI-Unterstützung die folgenden Methoden implementiert:
  
|**Statusobjekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystems  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Warteschlange  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
In **PR_RESOURCE_METHODS**kann eine oder mehrere der folgenden Werte festgelegt werden:
  
STATUS_CHANGE_PASSWORD 
  
> Gibt an, dass die [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) -Methode unterstützt wird. 
    
STATUS_FLUSH_QUEUES 
  
> Gibt an, dass die Methode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) unterstützt wird. 
    
STATUS_SETTINGS_DIALOG 
  
> Gibt an, dass [die SettingsDialog](imapistatus-settingsdialog.md) unterstützt wird. 
    
STATUS_VALIDATE_STATE 
  
> Gibt an, dass die Methode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) unterstützt wird. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

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

