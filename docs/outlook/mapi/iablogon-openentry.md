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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53dfb62bb33a4941e2b5627e729763101e24319d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791965"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Betrifft**: Outlook 
  
Öffnet einen Container, messaging-Benutzer oder eine Verteilerliste, und gibt einen Zeiger auf eine Implementierung Zugriff zu ermöglichen.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, messaging-Benutzer oder Verteilerliste zu öffnen.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle für den Zugriff auf die open-Objekt verwendet werden. Übergeben von NULL gibt den Bezeichner für das Objekt standard-Schnittstelle zurück. Für Container, ist der standard-Benutzeroberfläche [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Der Standard-Schnittstellen für Address Book-Objekten sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für ein messaging-Benutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet werden. Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mit Leseberechtigung geöffnet werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die **OpenEntry** -Methode erfolgreich, möglicherweise zurückgegeben werden, bevor der aufrufende Client vollständig Zugriff auf das Objekt hat. Wenn das Objekt nicht zugegriffen werden kann, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht davon ausgehen, dass die Lese-Schreib-Berechtigung gewährt wurde.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="remarks"></a>Hinweise

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder der Benutzer verfügt nicht über ausreichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein nur-Lese-Objekt mit Lese-/Schreibzugriff zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Die _LpEntryID_ angegebene Eintrags-ID stellt kein Objekts dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID in der _LpEntryID_ -Parameter ist nicht vom durch die Adressbuchanbieter erkanntes Format. 
    
## <a name="remarks"></a>Hinweise

MAPI-Aufrufen die **OpenEntry** -Methode, um einen Container öffnen messaging-Benutzer oder eine Verteilerliste. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Bevor Sie MAPI Ihrer **OpenEntry** -Methode aufruft, wird festgelegt, dass die Eintrags-ID in der _LpEntryID_ -Parameter für den Benutzer und nicht für einen anderen Anbieter gehört. MAPI wird durch entsprechende [MAPIUID](mapiuid.md) Strukturänderung in die Eintrags-ID mit der **MAPIUID** , die Sie durch Aufrufen der [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode beim Start registriert. 
  
Öffnen Sie das Objekt als schreibgeschützt, es sei denn, das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt ist. Wenn Sie die Änderung für das angeforderte Objekt nicht zulässig ist, keine überhaupt öffnen Sie das Objekt und zurückzugeben Sie MAPI_E_NO_ACCESS. 
  
Wenn MAPI NULL für _LpEntryID_übergibt, öffnen Sie den Stammcontainer in der Containerhierarchie.
  
Das Objekt, das Sie aufgefordert werden, öffnen Sie möglicherweise ein Objekt aus einem anderen Anbieter kopiert. In diesem Fall wird die Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. Wenn diese Eigenschaft auf das Objekt unterstützt, rufen Sie die [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) -Methode zum Binden von Code für diesen Eintrag in der fremden Anbieter auf und übergibt **PR_TEMPLATEID** in der _LpTemplateID_ -Parameter und den Wert 0 in die _ulTemplateFlags _Parameter. **IMAPISupport::OpenTemplateID** übergibt diese Informationen an den foreign Anbieter in einem Aufruf der fremde Anbieter [OpenTemplateID](iablogon-opentemplateid.md) -Methode. Wenn **IMAPISupport::OpenTemplateID** löst einen Fehler aus, in der Regel, da der fremde Anbieter nicht verfügbar ist oder nicht in das Profil enthalten ist versuchen Sie fortfahren, indem Sie den Eintrag ungebundenen als schreibgeschützt behandeln. Weitere Informationen zum Öffnen von Adressbucheinträgen fremden finden Sie unter [als ein Host-Adressbuchanbieter fungiert](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon: IUnknown](iablogoniunknown.md)

