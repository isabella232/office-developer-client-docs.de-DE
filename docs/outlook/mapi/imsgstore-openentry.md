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
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309695"
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird _._
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts oder NULL. Wenn _lpEntryID_ auf NULL festgelegt ist **** , öffnet OpenEntry den Stammordner für den Nachrichtenspeicher. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Das übergeben von NULL-Ergebnissen in der Standardschnittstelle des Objekts ([IMAPIFolder](imapifolderimapicontainer.md) für Ordner und [IMessage](imessageimapiprop.md) für Nachrichten) wird zurückgegeben. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert, dass das Objekt unter Verwendung der maximal für den Benutzer zulässigen Netzwerkberechtigungen und des maximalen Client Anwendungszugriffs geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mithilfe der Lese-/Schreibzugriff-Berechtigung geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte das Objekt mithilfe der Read-Only-Berechtigung geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wird. 
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_NO_CACHE
  
> Wenn ein Speicher im Cache-Modus geöffnet wird, kann ein Client oder Dienstanbieter **IMsgStore:: OpenEntry**aufrufen und das MAPI_NO_CACHE-Flag festlegen, um ein Element oder einen Ordner im Remotespeicher zu öffnen. Wenn Sie den Nachrichtenspeicher mit dem MDB_ONLINE-Flag auf dem Remoteserver öffnen, müssen Sie das MAPI_NO_CACHE-Flag nicht verwenden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: OpenEntry** -Methode öffnet einen Ordner oder eine Nachricht und gibt einen Zeiger auf eine Schnittstelle zurück, die für weiteren Zugriff verwendet werden kann. 
  
> [!IMPORTANT]
> Beim Öffnen von Ordnereinträgen in einem öffentlichen Informationsspeicher wie Ordner und Nachrichten verwenden Sie **IMsgStore:: OpenEntry** anstelle von [IMAPISession:: OpenEntry](imapisession-openentry.md). Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange-Konten in einem Profil definiert sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ordner und Nachrichten werden automatisch mit Schreibschutz Berechtigung geöffnet, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter fest. Durch Festlegen eines dieser Flags kann kein bestimmter Berechtigungstyp garantiert werden. die Berechtigungen, die Ihnen erteilt werden, hängen vom Nachrichtenspeicher Anbieter, der Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Obwohl **IMsgStore:: OpenEntry** zum Öffnen von Ordnern oder Nachrichten verwendet werden kann, ist es in der Regel schneller, die [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) -Methode zu verwenden, wenn Sie Zugriff auf den übergeordneten Ordner des Ordners oder der Nachricht haben, der geöffnet werden soll. 
  
Überprüfen Sie den Wert, der im _lpulObjType_ -Parameter zurückgegeben wird, um zu bestimmen, ob der zurückgegebene Objekttyp Ihren Erwartungen entspricht. Wenn der Objekttyp nicht der erwartete Typ ist, wandeln Sie den Zeiger vom _lppUnk_ -Parameter in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, werfen Sie _lppUnk_ in einen Zeiger vom Typ **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI verwendet die **IMsgStore:: OpenEntry** -Methode, um das Objekt zu öffnen, das einer EINTRAGS-ID zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

