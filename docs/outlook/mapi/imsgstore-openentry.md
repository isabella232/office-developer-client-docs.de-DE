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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792646"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Betrifft**: Outlook 
  
Öffnet einen Ordner oder eine Nachricht, und gibt einen Schnittstellenzeiger für den weiteren Zugriff. 
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf das durch den Parameter _LpEntryID_ _._
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des-Objekts zum Öffnen oder NULL. Wenn _LpEntryID_ auf NULL festgelegt ist, wird **OpenEntry** Stammordner für den Nachrichtenspeicher geöffnet. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, den Zugriff auf die geöffnete Objekt darstellt. Bei Übergabe von NULL führt das Objekt des standard-Schnittstelle ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner) und [IMessage](imessageimapiprop.md) für Nachrichten zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Werte können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt geöffnet werden, mithilfe der maximale Netzwerkberechtigungen für den Benutzer und die maximale Clientzugriff Anwendung zulässig. Wenn der Client über Lese-/Schreibberechtigung verfügt, sollte beispielsweise das Objekt geöffnet werden mithilfe von Lese-/Schreibberechtigung für; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mithilfe von schreibgeschützt geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_NO_CACHE
  
> Wenn ein Speichers im Cache-Modus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore::OpenEntry**, das MAPI_NO_CACHE-Flag zum Öffnen eines Elements oder einen Ordner auf dem remote-Speicher aufrufen. Wenn Sie den Nachrichtenspeicher mit dem MDB_ONLINE-Flag auf dem Remoteserver öffnen, müssen Sie nicht das Flag MAPI_NO_CACHE verwenden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::OpenEntry** -Methode öffnet ein Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle, die für eine zusätzliche Access verwendet werden kann. 
  
> [!IMPORTANT]
> Beim Öffnen der Einträge im Ordner in einem öffentlichen Speicher, wie Ordner und Nachrichten, verwenden Sie anstelle von [IMAPISession::OpenEntry](imapisession-openentry.md) **IMsgStore::OpenEntry** . Dadurch wird die Funktion für Öffentliche Ordner ordnungsgemäß sichergestellt, wenn in einem Profil mehrere Exchange-Konten definiert sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ordner und Nachrichten werden automatisch mit Leseberechtigung, geöffnet, es sei denn, Sie die Kennzeichen MAPI_MODIFY oder MAPI_BEST_ACCESS in der _UlFlags_ -Parameter festlegen. Festlegen einer dieser Flags garantiert keine bestimmte Art von Berechtigung. die Berechtigungen, die Sie erteilt werden, abhängig von der Nachricht Informationsdienst, Ihre Zugriffsebene und das Objekt ab. Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Obwohl **IMsgStore::OpenEntry** zum Öffnen eines beliebigen Ordners oder einer Nachricht verwendet werden können, ist es in der Regel schneller die [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) -Methode verwenden, wenn Sie haben Zugriff auf den übergeordneten Ordner des Ordners oder Nachricht geöffnet werden soll. 
  
Überprüfen Sie den Wert im _LpulObjType_ -Parameter bestimmt, ob der zurückgegebene Objekttyp ist, was Sie erwartet zurückgegeben. Wenn der Objekttyp nicht dem erwarteten Typ ist, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter. Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ **LPMAPIFOLDER**umgewandelt.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI (engl.) verwendet die **IMsgStore::OpenEntry** -Methode zum Öffnen des Objekts eines Eintrags-ID zugeordnet  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

