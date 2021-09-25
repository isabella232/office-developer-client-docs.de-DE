---
title: PidTagResourceMethods (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df8b1b855206a88044114c0d86bda3dd9b609aa1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604257"
---
# <a name="pidtagresourcemethods-canonical-property"></a>PidTagResourceMethods (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Methoden in der **IMAPIStatus-Schnittstelle** angeben, die vom Statusobjekt unterstützt werden. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Kennung:  <br/> |0x3E02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt an, welche der Methoden in der Implementierung von **IMAPIStatus** eines Statusobjekts unterstützt werden. Statusobjekte dürfen MAPI_E_NO_SUPPORT von nicht unterstützten Methoden zurückgeben. 
  
Clients verwenden **die PR_RESOURCE_METHODS-Eigenschaft** eines Statusobjekts, um Aufrufe nicht unterstützter Methoden zu vermeiden. Wenn das Flag, das einer bestimmten Methode entspricht, festgelegt ist, ist die Methode vorhanden und kann aufgerufen werden. Wenn dieses Kennzeichen eindeutig ist, sollte die Methode nicht aufgerufen werden. 
  
Die von der MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Mindestens eines der folgenden Flags kann in **PR_RESOURCE_METHODS** festgelegt werden:
  
STATUS_CHANGE_PASSWORD 
  
> Gibt an, dass die [IMAPIStatus::ChangePassword-Methode](imapistatus-changepassword.md) unterstützt wird. 
    
STATUS_FLUSH_QUEUES 
  
> Gibt an, dass die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) unterstützt wird. 
    
STATUS_SETTINGS_DIALOG 
  
> Gibt an, dass die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) unterstützt wird. 
    
STATUS_VALIDATE_STATE 
  
> Gibt an, dass die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) unterstützt wird. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

