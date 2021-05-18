---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409230"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff zu ermöglichen.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des zu öffnende Containers, Messagingbenutzers oder Verteilerlistens.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Durch Übergeben von NULL wird der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben. Für Container ist die Standardschnittstelle [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht der **OpenEntry-Methode,** erfolgreich zurückzukehren, möglicherweise bevor der aufrufende Client vollständig auf das Objekt zugegriffen hat. Wenn nicht auf das Objekt zugegriffen wird, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollten nicht davon ausgehen, dass Lese-/Schreibberechtigungen erteilt wurden.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="remarks"></a>Hinweise

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder verfügt der Benutzer nicht über ausreichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Der von  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner im  _lpEntryID-Parameter_ hat kein vom Adressbuchanbieter erkanntes Format. 
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **OpenEntry-Methode** auf, um einen Container, einen Messagingbenutzer oder eine Verteilerliste zu öffnen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Bevor MAPI Ihre **OpenEntry-Methode** aufruft, bestimmt sie, dass der Eintragsbezeichner im  _lpEntryID-Parameter_ zu Ihnen und nicht zu einem anderen Anbieter gehört. MAPI führt dies durch Abgleichen der [MAPIUID-Struktur](mapiuid.md) in der Eintrags-ID mit der **MAPIUID** aus, die Sie beim Start durch Aufrufen der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) registriert haben. 
  
Öffnen Sie das Objekt als schreibgeschützt, es sei denn, MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter festgelegt_ ist. Wenn Sie keine Änderung für das angeforderte Objekt zulassen, öffnen Sie das Objekt überhaupt nicht, und geben Sie MAPI_E_NO_ACCESS. 
  
Wenn MAPI NULL für  _lpEntryID übergibt,_ öffnen Sie den Stammcontainer in der Containerhierarchie.
  
Das Objekt, das Sie öffnen möchten, kann ein Objekt sein, das von einem anderen Anbieter kopiert wurde. In diesem Fall wird die PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. Wenn das Objekt diese Eigenschaft unterstützt, rufen Sie die [IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf, um eine Bindung an Code für diesen Eintrag im fremden Anbieter zu erstellen. Übergeben Sie **PR_TEMPLATEID** im _lpTemplateID-Parameter_ und 0 im _ulTemplateFlags-Parameter._ **IMAPISupport::OpenTemplateID** übergibt diese Informationen an den fremden Anbieter in einem Aufruf der [IABLogon::OpenTemplateID-Methode](iablogon-opentemplateid.md) des fremden Anbieters. Wenn **IMAPISupport::OpenTemplateID** einen Fehler verursacht, in der Regel, da der fremde Anbieter nicht verfügbar ist oder nicht im Profil enthalten ist, versuchen Sie, den Ungebundenen Eintrag als schreibgeschützt zu behandeln. Weitere Informationen zum Öffnen von fremden Adressbucheinträgen finden Sie unter [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon : IUnknown](iablogoniunknown.md)

