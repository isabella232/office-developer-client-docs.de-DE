---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e41952a4a725ab8368eb4c4b23c3ff3044377f4d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600992"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf Verteilerlisten in modifizierbaren Adressbuchcontainern. **IDistList** kann Verteilerlisten zusätzlich zur Namensauflösung erstellen, kopieren und löschen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Verteilerlistenobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IDistList  <br/> |
|Zeigertyp:  <br/> |LPDISTLIST  <br/> |
|Transaktionsmodell:  <br/> |Transaktiven  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **IDistList-Schnittstelle** erbt von [IMAPIContainer](imapicontainerimapiprop.md) und enthält die gleichen Methoden wie Adressbuchcontainer. Da die Methoden der **IDistList-Schnittstelle** mit denen der [IABContainer-Schnittstelle](iabcontainerimapicontainer.md) identisch sind, werden sie hier nicht dupliziert. 
  
Eine Verteilerliste oder ein Objekt, das **IDistList** implementiert, ist eine Auflistung von Nachrichtenbenutzerobjekten oder einzelnen Empfängern. Eine Verteilerliste kann aus allen Nachrichtenbenutzerobjekten oder aus einigen Nachrichtenbenutzern und einigen Verteilerlisten bestehen. 
  
Es gibt in der Regel zwei Arten von Verteilerlisten:
  
- Verteilerlisten, die durch das zugrunde liegende Messagingsystem erweitert werden. Dieser Listentyp hat eine Adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), und wird genauso behandelt, als ob es sich um einen einzelnen Empfänger handeln würde. 
    
- Verteilerlisten, die in einem lokalen Container vorhanden sind und um die Clientanwendung erweitert werden.
    
Zu den optionalen Verteilerlisteneigenschaften gehören:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Beachten Sie, dass **PR_ADDRTYPE** erforderlich ist, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) jedoch nicht. Der Grund dafür ist, dass eine Verteilerliste ohne E-Mail-Adresse weiterhin Nachrichten empfangen kann, deren Mitgliederliste jedoch erweitert werden muss. Wenn die **PR_ADDRTYPE-Eigenschaft** auf MAPIPDL festgelegt ist, führt MAPI die Erweiterung aus. Wenn **PR_ADDRTYPE** ein anderer Wert als MAPIPDL ist, führt der Transportanbieter die Erweiterung aus. 
  
Weitere Informationen zur Verwendung der **IDistList** -Methoden finden Sie in den Referenzeinträgen für die parallelen Methoden von **IABContainer**.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

