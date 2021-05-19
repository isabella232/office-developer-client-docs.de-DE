---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409615"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück. 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle des Objekts zurückgegeben wird. Wenn das zu öffnende Objekt z. B. eine Nachricht ist, lautet die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulOpenFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximalen Netzwerkberechtigungen geöffnet wird, die für den Aufrufer zulässig sind. Wenn der Aufrufer beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt als Lese-/Schreibzugriff geöffnet werden. Wenn der Aufrufer über schreibgeschützte Berechtigungen verfügt, sollte das Objekt als schreibgeschützt geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor auf das Objekt vollständig für den Aufrufer zugegriffen werden kann. Wenn auf das Objekt nicht zugegriffen werden kann, kann ein nachfolgender Objektaufruf zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Dem Eintragsbezeichner, der im  _lpEntryID-Parameter_ übergeben wird, ist kein Objekt zugeordnet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner hat ein nicht wiedererkennbares Format. Dieser Wert wird in der Regel zurückgegeben, wenn der Adressbuchanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenEntry-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **IMAPISupport::OpenEntry auf,** um einen Zeiger auf eine Schnittstelle abzurufen, die für den Zugriff auf ein bestimmtes Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie IMAPISupport::OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [stattdessen IMsgStore::OpenEntry](imsgstore-openentry.md) auf. Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook::OpenEntry auf.](iaddrbook-openentry.md) Diese spezifischere Methoden sind schneller als **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** öffnet alle Objekte als schreibgeschützt, es sei denn, Sie legen das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ ein, und Ihre Berechtigungen sind ausreichend. Das Festlegen eines dieser Kennzeichen garantiert keine bestimmte Art von Zugriff. Die Ihnen erteilten Berechtigungen hängen von Ihrer Zugriffsebene, dem Objekt und dem Dienstanbieter ab, der das Objekt besitzt. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
Überprüfen Sie den im  _lpulObjType-Parameter_ zurückgegebenen Wert, um zu ermitteln, ob der zurückgegebene Objekttyp den erwarteten Wert hat. Wenn der Objekttyp wie erwartet ist, wird der Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs umgekippt. Wenn Sie z. B. einen Ordner öffnen, wird  _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER verschoben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

