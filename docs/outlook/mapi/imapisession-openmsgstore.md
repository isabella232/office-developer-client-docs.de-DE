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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418022"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für weiteren Zugriff zurück. 
  
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
  
> [in] Ein Handle zum übergeordneten Fenster des Dialogfelds allgemeine Adresse und andere zugehörige Displays.
    
_cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
_lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des zu öffnende Nachrichtenspeichers. Der  _lpEntryID-Parameter_ darf nicht NULL sein. 
    
_lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Nachrichtenspeicher verwendet werden soll. Durch Übergeben von NULL gibt  _der lppMDB-Parameter_ einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher zurück (**IMsgStore**).
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können verwendet werden:
    
  - MAPI_BEST_ACCESS: Fordert an, dass der Nachrichtenspeicher mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und den maximalen Clientanwendungsberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte der Nachrichtenspeicher mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte der Nachrichtenspeicher mit schreibgeschützter Berechtigung geöffnet werden. 
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht **es OpenMsgStore,** erfolgreich zurückzukehren, möglicherweise bevor der Nachrichtenspeicher vollständig für den aufrufenden Client verfügbar ist. Wenn der Nachrichtenspeicher nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden. 
      
  - MDB \_ NO_DIALOG: Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Kennzeichen festgelegt ist und **OpenMsgStore** nicht über ausreichende Konfigurationsinformationen verfügt, um den Nachrichtenspeicher ohne Hilfe des Benutzers zu öffnen, wird MAPI_E_LOGON_FAILED. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer zum Korrigieren eines Namens oder Kennworts oder zum Ausführen anderer Aktionen zum Herstellen einer Verbindung mit dem Nachrichtenspeicher aufgefordert. 
      
  - MDB NO_MAIL: Der Nachrichtenspeicher sollte nicht zum Senden oder Empfangen \_ von E-Mails verwendet werden. Wenn dieses Flag festgelegt ist, benachrichtigt MAPI den MAPI-Spooler nicht darüber, dass dieser Nachrichtenspeicher geöffnet wird.
      
  - MDB ONLINE: Im Cache-Exchange-Modus kann ein Client oder Dienstanbieter diese Methode mit MDB_ONLINE aufrufen, um die Verbindung zum lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver \_ zu öffnen. Sie können einen Exchange im Cachemodus und im nicht zwischengespeicherten Modus nicht gleichzeitig in derselben MAPI-Sitzung öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.
      
  - MDB_TEMPORARY: Die MAPI wird angewiesen, dass der Nachrichtenspeicher nicht dauerhaft ist und nicht der Nachrichtenspeichertabelle hinzugefügt werden sollte. Dieses Flag wird zum Anmelden am Nachrichtenspeicher verwendet, damit Informationen programmgesteuert aus dem Profilabschnitt abgerufen werden können. 
      
  - MDB_WRITE: Fordert Lese-/Schreibberechtigungen für den Nachrichtenspeicher an.
    
_lppMDB_
  
> [out] Zeiger auf einen Zeiger des Nachrichtenspeichers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Nachrichtenspeicher zu zugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der durch  _lpEntryID_ angegebene Nachrichtenspeicher ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Locale-Informationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf ist erfolgreich, der Nachrichtenspeicheranbieter verfügt jedoch über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter zu erhalten. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::OpenMsgStore-Methode** öffnet einen bestimmten Nachrichtenspeicher. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt. Wenn Sie das MDB_WRITE festlegen, erhalten Sie möglicherweise keine Lese-/Schreibberechtigung. Die letzte Zugriffsebene, die MAPI dem Nachrichtenspeicher zuteil wird, hängt von Ihrer Berechtigungsstufe, dem Nachrichtenspeicher selbst und dem Nachrichtenspeicheranbieter ab. 
  
Wenn Sie **OpenMsgStore aufrufen,** um einen Nachrichtenspeicher mit schreibgeschützter Berechtigung zu öffnen, tritt Folgendes auf: 
  
- Die **\_ PR-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Speichers verfügt nicht über die \_ STORE-MODIFY_OK und store \_ CREATE_OK Bits. 
    
- Aufrufe zum Öffnen einer der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPISession::OpenEntry](imapisession-openentry.md) mit dem MAPI_MODIFY werden fehlschlagen. 
    
- Aufrufe zum Öffnen einer der Eigenschaften der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit dem MAPI_MODIFY werden fehlschlagen. 
    
- Aufrufe einer der folgenden Methoden führen zu einem Fehler: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Aufrufe der folgenden Methoden führen zu einem Fehler, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, ob das Ziel mit dem Quellnachrichtenspeicher identisch ist oder ein anderer schreibgeschützter Speicher ist.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI verwendet die **IMAPISession::OpenMsgStore-Methode,** um einen Nachrichtenspeicher zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
- [Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

