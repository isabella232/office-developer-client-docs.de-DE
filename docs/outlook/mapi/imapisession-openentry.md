---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426387"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Wenn das zu öffnende Objekt z. B. eine Nachricht ist, lautet die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximalen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden. 
    
MAPI_CACHE_OK
  
> Verwenden Sie alle Mittel, einschließlich Offlineadressbüchern, um die Namensauflösung durchzuführen.
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Objektaufruf einen Fehler verursachen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt werden. 
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht, um die Namensauflösung durchzuführen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
SHOW_SOFT_DELETES
  
> Elemente anzeigen, die derzeit als "soft deleted" markiert sind (d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente).
    
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
  
> Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner hat ein nicht wiedererkennbares Format. Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::OpenEntry-Methode** öffnet einen Nachrichtenspeicher oder ein Adressbuchobjekt und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf das Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

> [!IMPORTANT]
> Verwenden Sie beim Öffnen von Ordnereinträgen in einem öffentlichen Speicher, z. B. Ordner und Nachrichten, [IMsgStore::OpenEntry](imsgstore-openentry.md) anstelle **von IMAPISession::OpenEntry**. Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn Exchange konten in einem Profil definiert sind. 
  
Rufen **Sie IMAPISession::OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [IMsgStore::OpenEntry auf.](imsgstore-openentry.md) Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook::OpenEntry auf.](iaddrbook-openentry.md) Diese spezifischere Methode ist schneller als **IMAPISession::OpenEntry**. 
  
MAPI öffnet alle Objekte mit schreibgeschützter Berechtigung, es sei denn, Sie legen das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _ulFlags-Parameter._ Das Festlegen eines dieser Kennzeichen garantiert keine bestimmte Art von Zugriff. Die erteilten Berechtigungen hängen vom Dienstanbieter, der Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft ab.
  
Das Aufrufen von **IMAPISession::OpenEntry** und festlegen, dass  _lpEntryID_ auf den Eintragsbezeichner eines Nachrichtenspeichers zeigt, ist identisch mit dem Aufrufen der [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) mit dem MDB_NO_DIALOG-Flagsatz. Die Kennzeicheneinstellungen sind ebenfalls äquivalent, mit der Ausnahme, dass Sie zum Anfordern von Lese-/Schreibberechtigungen mit **OpenMsgStore** das MDB_WRITE-Flag anstatt MAPI_MODIFY. 
  
Überprüfen Sie den im  _lpulObjType-Parameter_ zurückgegebenen Wert, um zu ermitteln, ob der zurückgegebene Objekttyp den erwarteten Wert hat. Wenn der Objekttyp nicht der erwartete Typ ist, wird der Zeiger vom  _lppUnk-Parameter_ in einen Zeiger des entsprechenden Typs umgekippt. Wenn Sie z. B. einen Ordner öffnen, wird  _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER verschoben. 
  
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

