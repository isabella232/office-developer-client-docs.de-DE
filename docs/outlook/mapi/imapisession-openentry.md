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
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591015"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für zusätzliche Zugriff.
  
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
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, den Zugriff auf die geöffnete Objekt darstellt. Übergeben von NULL gibt Standardschnittstelle für das Objekt zurück. Wenn das Objekt geöffnet werden soll, eine Nachricht ist, ist der standard-Benutzeroberfläche beispielsweise [IMessage](imessageimapiprop.md); Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die standard-Schnittstellen für Address Book-Objekten sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für ein messaging-Benutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Werte können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt geöffnet werden, mithilfe der maximale Netzwerkberechtigungen für den Benutzer und die maximale Clientzugriff Anwendung zulässig. Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte das Objekt mit Leseberechtigung geöffnet werden. 
    
MAPI_CACHE_OK
  
> Verwenden Sie alle Mittel, einschließlich Offlineadressbücher, um namensauflösung auszuführen.
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann nachfolgende Objekt anrufen verursacht einen Fehler. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht namensauflösung ausführen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
SHOW_SOFT_DELETES
  
> Anzeigen der Elemente, die aktuell als soft markiert werden gelöscht (d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase).
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt zugeordneten die Eintrags-ID in der _LpEntryID_ -Parameter übergeben. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben wird in einem Format nicht erkannt. Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält nicht geöffnet ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Zugriff auf das Objekt, können die **IMAPISession::OpenEntry** -Methode wird geöffnet, eine Nachricht speichern oder address Book-Objekt zurückgeben einem Zeiger auf eine Schnittstelle, die, verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

> [!IMPORTANT]
> Beim Öffnen der Einträge im Ordner in einem öffentlichen Speicher, wie Ordner und Nachrichten, verwenden Sie anstelle von **IMAPISession::OpenEntry** [IMsgStore::OpenEntry](imsgstore-openentry.md) . Dadurch wird die Funktion für Öffentliche Ordner ordnungsgemäß sichergestellt, wenn in einem Profil mehrere Exchange-Konten definiert sind. 
  
Rufen Sie **IMAPISession::OpenEntry** nur, wenn Sie nicht über welche Art Objekt kennen, die Sie öffnen möchten. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen möchten, rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md). Wenn Sie wissen, dass Sie ein Adressbuchcontainer öffnen möchten, rufen Sie ein messaging-Benutzer oder eine Verteilerliste, [IAddrBook::OpenEntry](iaddrbook-openentry.md). Diese bestimmten Methoden sind schneller als **IMAPISession::OpenEntry**. 
  
MAPI öffnet alle Objekte mit Leseberechtigung, es sei denn, Sie das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS im _UlFlags_ -Parameter festgelegt. Festlegen einer dieser Flags garantiert keine bestimmte Art von Zugriff. die Berechtigungen, die erteilt werden, hängt von der Dienstanbieter, die Zugriffsebene und das Objekt ab. Rufen Sie zum Bestimmen der Zugriffsebene des geöffneten-Objekts, dessen **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Aufrufen von **IMAPISession::OpenEntry** und Einstellung _LpEntryID_ So zeigen Sie auf die Eintrags-ID des einen Nachrichtenspeicher ist identisch mit Aufrufen der [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode mit dem MDB_NO_DIALOG-Flag festgelegt. Die Kennzeichnung Einstellungen sind auch entspricht, es sei denn, die Berechtigung Lese-/Schreibzugriff mit **OpenMsgStore**, muss das Flag MDB_WRITE anstelle von MAPI_MODIFY festgelegt werden. 
  
Überprüfen Sie den Wert in der _LpulObjType_ -Parameter, um festzustellen, ob der Objekttyp zurückgegeben wird, was Sie erwartet zurückgegeben. Wenn der Objekttyp nicht den Typ, den Sie erwartet ist, wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs aus dem _LppUnk_ -Parameter. Angenommen, wenn Sie einen Ordner öffnen, _LppUnk_ auf einen Zeiger vom Typ LPMAPIFOLDER umgewandelt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::OpenEntry** -Methode zum Öffnen eines Objekts an.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

