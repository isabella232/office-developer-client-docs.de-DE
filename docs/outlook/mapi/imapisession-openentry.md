---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4cde3fb71eeccd82042787e329f96309eaffa8c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596176"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für zusätzlichen Zugriff zurück.
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Objekts.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts zurückgegeben. Wenn das zu öffnende Objekt z. B. eine Nachricht ist, ist die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist dies [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mithilfe der für den Benutzer maximal zulässigen Netzwerkberechtigungen und des maximalen Clientanwendungszugriffs geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden. 
    
MAPI_CACHE_OK
  
> Verwenden Sie alle Mittel, einschließlich Offlineadressbüchern, um die Namensauflösung durchzuführen.
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt für den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objektaufrufs einen Fehler verursachen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wird. 
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung auszuführen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
SHOW_SOFT_DELETES
  
> Anzeigen von Elementen, die derzeit als vorläufig gelöscht markiert sind (d. a. sie befinden sich in der Aufbewahrungszeitphase für gelöschte Elemente).
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt mit dem Eintragsbezeichner verknüpft, der im  _lpEntryID-Parameter_ übergeben wird. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner weist ein nicht erkennbares Format auf. Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::OpenEntry-Methode** öffnet ein Nachrichtenspeicher- oder Adressbuchobjekt und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf das Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

> [!IMPORTANT]
> Verwenden Sie beim Öffnen von Ordnereinträgen in einem öffentlichen Speicher, z. B. Ordner und Nachrichten, [IMsgStore::OpenEntry](imsgstore-openentry.md) anstelle von **IMAPISession::OpenEntry.** Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange Konten in einem Profil definiert sind. 
  
Rufen Sie **IMAPISession::OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md)auf. Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf. Diese spezifischeren Methoden sind schneller als **IMAPISession::OpenEntry**. 
  
MAPI öffnet alle Objekte mit schreibgeschützter Berechtigung, es sei denn, Sie legen das flag MAPI_MODIFY oder MAPI_BEST_ACCESS im  _ulFlags-Parameter_ fest. Das Festlegen eines dieser Flags garantiert keinen bestimmten Zugriffstyp. Die erteilten Berechtigungen hängen vom Dienstanbieter, der Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
Das Aufrufen von **IMAPISession::OpenEntry** und das Festlegen von  _lpEntryID,_ um auf den Eintragsbezeichner eines Nachrichtenspeichers zu zeigen, entspricht dem Aufrufen der [IMAPISession::OpenMsgStore-Methode,](imapisession-openmsgstore.md) für die das MDB_NO_DIALOG Flag festgelegt ist. Die Flageinstellungen sind ebenfalls gleichwertig, mit der Ausnahme, dass Sie zum Anfordern der Lese-/Schreibberechtigung für **OpenMsgStore** das MDB_WRITE-Flag anstelle von MAPI_MODIFY festlegen müssen. 
  
Überprüfen Sie den im  _lpulObjType-Parameter_ zurückgegebenen Wert, um festzustellen, ob der zurückgegebene Objekttyp dem erwarteten Entspricht. Wenn es sich bei dem Objekttyp nicht um den erwarteten Typ handelt, wandeln Sie den Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, wandeln Sie  _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER um. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI verwendet die **IMAPISession::OpenEntry-Methode,** um ein Objekt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

