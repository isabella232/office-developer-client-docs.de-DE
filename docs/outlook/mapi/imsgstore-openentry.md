---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409335"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück. 
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_  _verweist._
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts oder NULL. Wenn  _lpEntryID_ auf NULL festgelegt ist, öffnet **OpenEntry** den Stammordner für den Nachrichtenspeicher. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle des Objekts ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner und [IMessage](imessageimapiprop.md) für Nachrichten) zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximalen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mithilfe der Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt werden. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_NO_CACHE
  
> Wenn ein Speicher im Cachemodus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore::OpenEntry** aufrufen und das flag MAPI_NO_CACHE festlegen, um ein Element oder einen Ordner im Remotespeicher zu öffnen. Wenn Sie den Nachrichtenspeicher mit dem MDB_ONLINE auf dem Remoteserver öffnen, müssen Sie das MAPI_NO_CACHE verwenden.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::OpenEntry-Methode** öffnet einen Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle zurück, die für weiteren Zugriff verwendet werden kann. 
  
> [!IMPORTANT]
> Verwenden Sie beim Öffnen von Ordnereinträgen in einem öffentlichen Speicher, z. B. Ordner und Nachrichten, **IMsgStore::OpenEntry** anstelle [von IMAPISession::OpenEntry](imapisession-openentry.md). Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn Exchange konten in einem Profil definiert sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ordner und Nachrichten werden automatisch mit schreibgeschützter Berechtigung geöffnet, es sei denn, Sie legen MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ ein. Das Festlegen eines dieser Kennzeichen garantiert keinen bestimmten Berechtigungstyp. Die ihnen erteilten Berechtigungen hängen vom Nachrichtenspeicheranbieter, der Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
Obwohl **IMsgStore::OpenEntry** zum Öffnen eines beliebigen Ordners oder einer Nachricht verwendet werden kann, ist es in der Regel schneller, die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) zu verwenden, wenn Sie Zugriff auf den übergeordneten Ordner des zu öffnenden Ordners oder der Zu öffnenden Nachricht haben. 
  
Überprüfen Sie den im  _lpulObjType-Parameter_ zurückgegebenen Wert, um zu ermitteln, ob der zurückgegebene Objekttyp den erwarteten Wert hat. Wenn der Objekttyp nicht der erwartete Typ ist, wird der Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs umgekippt. Wenn Sie z. B. einen Ordner öffnen, wird _lppUnk_ in einen Zeiger vom Typ **LPMAPIFOLDER verschoben.**
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI verwendet die **IMsgStore::OpenEntry-Methode,** um das Objekt zu öffnen, das einer Eintrags-ID zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

