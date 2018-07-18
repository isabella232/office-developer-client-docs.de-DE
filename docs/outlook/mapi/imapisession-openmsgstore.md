---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792322"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Betrifft**: Outlook 
  
Öffnet einen Nachrichtenspeicher und gibt einen Zeiger [IMsgStore](imsgstoreimapiprop.md) für den weiteren Zugriff. 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameter

_ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Adresse Standarddialogfeld und anderer weiterführende zeigt.
    
_cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
_lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers geöffnet werden soll. Der Parameter _LpEntryID_ darf nicht NULL sein. 
    
_lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellenbezeichner (IID), der die Schnittstelle für verwendet werden, um die Nachrichtenspeicher zugreifen darstellt. Übergeben von NULL bewirkt, dass den _LppMDB_ -Parameter, um einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher (**IMsgStore**) zurückzugeben.
    
_ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Werte können verwendet werden:
    
  - MAPI_BEST_ACCESS: Fordert, dass der Nachrichtenspeicher mit den Netzwerkberechtigungen maximale geöffnet werden zulässig für den Benutzer und die maximale Client Anwendungsberechtigungen. Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, der Nachrichtenspeicher mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client nur-Lese-Berechtigung verfügt, sollte der Nachrichtenspeicher mit Leseberechtigung geöffnet werden. 
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht **OpenMsgStore** zurückgegeben wurde, ist möglicherweise vor der Meldung Store an den aufrufenden Client vollständig verfügbar. Wenn der Nachrichtenspeicher nicht verfügbar ist, kann die nachfolgende Objekt Anrufen ein Fehler ausgelöst. 
      
  - MDB\_NO_DIALOG: verhindert, dass die Anzeige von Dialogfeldern für die Anmeldung. Wenn dieses Flag festgelegt ist, und **OpenMsgStore** hat nicht genügend Konfigurationsinformationen des Nachrichtenspeichers ohne die Benutzer Hilfe öffnen, wird die MAPI_E_LOGON_FAILED zurückgegeben. Wenn dieses Flag nicht festgelegt ist, kann der Nachricht Speicheranbieter auffordern, um einen Namen oder das Kennwort zu korrigieren oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Nachrichtenspeicher benötigt werden. 
      
  - MDB\_NO_MAIL: Nachrichtenspeicher sollte nicht für das Senden oder Empfangen von e-Mail verwendet werden. Wenn dieses Flag festgelegt ist, benachrichtigt MAPI nicht der MAPI-Warteschlange, dass dieses Nachrichtenspeichers geöffnet wird.
      
  - MDB\_ONLINE: In Cached Exchange Mode ein Client oder Dienstanbieter kann diese Methode mit MDB_ONLINE Überschreiben der Verbindungs mit den lokalen Nachrichtenspeicher und öffnen Sie den Speicher auf dem Remoteserver aufrufen. Sie können keinen Exchange-Speicher gleichzeitig in derselben MAPI-Sitzung im Cache-Modus und im nicht-Cache-Modus öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie dieses Flag zu öffnen, oder öffnen eine neue MAPI-Sitzung, in dem Sie den Exchange-Speicher auf dem Remoteserver mithilfe dieses Flag öffnen können.
      
  - MDB_TEMPORARY: Weist MAPI an, dass der Nachrichtenspeicher ist jedoch nicht dauerhaft und nicht die Nachricht Store-Tabelle hinzugefügt werden sollte. Dieses Kennzeichen werden verwendet, um den Nachrichtenspeicher anmelden, damit Informationen aus dem Profilabschnitt programmgesteuert abgerufen werden kann. 
      
  - MDB_WRITE: Anforderungen Lese-/Schreibberechtigung auf den Nachrichtenspeicher.
    
_lppMDB_
  
> [out] Zeiger auf einen Zeiger des Nachrichtenspeichers.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Nachrichtenspeicher zugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der Nachrichtenspeicher angegeben durch _LpEntryID_ ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht zur Unterstützung der Codeseite für den Client konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht konfiguriert, um Gebietsschemainformationen des Clients zu unterstützen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachricht Speicheranbieter hat Fehlerinformationen verfügbar. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Wenn Sie die Fehlerinformationen vom Anbieter erhalten möchten, rufen Sie die [IMAPISession::GetLastError](imapisession-getlasterror.md) -Methode. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::OpenMsgStore** -Methode wird die einen bestimmten Nachrichtenspeicher geöffnet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt. Wenn Sie das MDB_WRITE-Flag festlegen, können Sie noch nicht Lese-/Schreibberechtigung erteilt werden. Die endgültige Zugriffsebene, die MAPI-weist mit dem Nachrichtenspeicher hängt von Ihrer Berechtigungsstufe, die Nachricht selbst und die Nachricht Speicheranbieter gespeichert. 
  
Wenn Sie **OpenMsgStore** zum Öffnen eines Nachrichtenspeichers mit Leseberechtigung aufrufen, geschieht Folgendes: 
  
- Des Speichers **PR\_STORE_SUPPORT_MASK** -Eigenschaft ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) haben keinen dessen Speicher\_MODIFY_OK und STORE\_CREATE_OK bits festlegen. 
    
- Anrufe an des Nachrichtenspeicher Nachrichten oder Ordner öffnen, indem Sie [IMAPISession::OpenEntry](imapisession-openentry.md) mit dem Flag MAPI_MODIFY schlägt fehl. 
    
- Anrufe an eine der Eigenschaften des Nachrichtenspeicher Nachrichten oder Ordner öffnen, indem Sie das Kennzeichen MAPI_MODIFY [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit schlägt fehl. 
    
- Aufrufe an eine der folgenden Methoden schlagen fehl: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Aufrufe der folgenden Methoden schlägt fehl, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, ob das Ziel identisch mit der Quelle Nachrichtenspeicher ist oder einen anderen nur-Lese-Speicher.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::OpenMsgStore** -Methode, um einen Nachrichtenspeicher zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
- [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

