---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cab25a6d0e54490f3f5364e3c5d40fec1584a6de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571668"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück. 
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Objekts oder NULL. Wenn  _lpEntryID_ auf NULL festgelegt ist, öffnet **OpenEntry** den Stammordner für den Nachrichtenspeicher. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner und [IMessage](imessageimapiprop.md) für Nachrichten) zurückgegeben. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mithilfe der für den Benutzer maximal zulässigen Netzwerkberechtigungen und des maximalen Clientanwendungszugriffs geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mithilfe der Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mithilfe der schreibgeschützten Berechtigung geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt für den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objektaufrufs einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wird. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_NO_CACHE
  
> Wenn ein Speicher im Cachemodus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore::OpenEntry** aufrufen und das flag MAPI_NO_CACHE festlegen, um ein Element oder einen Ordner im Remotespeicher zu öffnen. Wenn Sie den Nachrichtenspeicher mit dem Flag MDB_ONLINE auf dem Remoteserver öffnen, müssen Sie nicht das flag MAPI_NO_CACHE verwenden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::OpenEntry-Methode** öffnet einen Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle zurück, die für weiteren Zugriff verwendet werden kann. 
  
> [!IMPORTANT]
> Verwenden Sie beim Öffnen von Ordnereinträgen in einem öffentlichen Speicher, z. B. Ordner und Nachrichten, **IMsgStore::OpenEntry** anstelle von [IMAPISession::OpenEntry.](imapisession-openentry.md) Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange Konten in einem Profil definiert sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ordner und Nachrichten werden automatisch mit schreibgeschützter Berechtigung geöffnet, es sei denn, Sie legen das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ fest. Das Festlegen eines dieser Flags garantiert keinen bestimmten Berechtigungstyp. Welche Berechtigungen Ihnen erteilt werden, hängt vom Nachrichtenspeicheranbieter, Ihrer Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
**Obwohl IMsgStore::OpenEntry** zum Öffnen eines beliebigen Ordners oder einer Nachricht verwendet werden kann, ist es in der Regel schneller, die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) zu verwenden, wenn Sie Zugriff auf den übergeordneten Ordner des ordners oder der Nachricht haben, der geöffnet werden soll. 
  
Überprüfen Sie den im  _Parameter "lpulObjType"_ zurückgegebenen Wert, um festzustellen, ob der zurückgegebene Objekttyp dem erwarteten entspricht. Wenn der Objekttyp nicht der erwartete Typ ist, wandeln Sie den Zeiger aus dem  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, wandeln Sie  _lppUnk_ in einen Zeiger vom Typ **LPMAPIFOLDER** um.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI verwendet die **IMsgStore::OpenEntry-Methode,** um das einer Eintrags-ID zugeordnete Objekt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

