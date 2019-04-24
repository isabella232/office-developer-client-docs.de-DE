---
title: Kanonische Pidtagresourcemethods (-Eigenschaft
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
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330142"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Kanonische Pidtagresourcemethods (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die die Methoden in der **IMAPIStatus** -Schnittstelle, die vom Status-Objekt unterstützt werden. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Kennung:  <br/> |0x3E02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, welche der Methoden in der Implementierung von **IMAPIStatus** eines Status Objekts unterstützt werden. Status-Objekte können MAPI_E_NO_SUPPORT von nicht unterstützten Methoden zurückgeben. 
  
Clients verwenden die **PR_RESOURCE_METHODS** -Eigenschaft eines Status Objekts, um das Aufrufen von nicht unterstützten Methoden zu vermeiden. Wenn das Flag für eine bestimmte Methode festgelegt ist, ist die Methode vorhanden und kann aufgerufen werden. Wenn dieses Flag leer ist, sollte die Methode nicht aufgerufen werden. 
  
Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Eine oder mehrere der folgenden Flags können in **PR_RESOURCE_METHODS**festgelegt werden:
  
STATUS_CHANGE_PASSWORD 
  
> Gibt an, dass die [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) -Methode unterstützt wird. 
    
STATUS_FLUSH_QUEUES 
  
> Gibt an, dass die [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode unterstützt wird. 
    
STATUS_SETTINGS_DIALOG 
  
> Gibt an, dass die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode unterstützt wird. 
    
STATUS_VALIDATE_STATE 
  
> Gibt an, dass die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode unterstützt wird. 
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

