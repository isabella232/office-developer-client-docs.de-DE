---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd6b0fd6c080e9d8dfe25b5e1a1773bc563efb89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575855"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für den weiteren Zugriff zurück. 
  
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
  
> [in] Ein Handle für das übergeordnete Fenster des allgemeinen Adressdialogfelds und anderer verwandter Anzeigen.
    
_cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
_lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Nachrichtenspeichers. Der  _lpEntryID-Parameter_ darf nicht NULL sein. 
    
_lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Nachrichtenspeicher verwendet werden soll. Wenn NULL übergeben wird, gibt der  _lppMDB-Parameter_ einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher zurück (**IMsgStore**).
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
  - MAPI_BEST_ACCESS: Fordert an, dass der Nachrichtenspeicher mit den für den Benutzer maximal zulässigen Netzwerkberechtigungen und den maximalen Clientanwendungsberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte der Nachrichtenspeicher mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte der Nachrichtenspeicher mit schreibgeschützter Berechtigung geöffnet werden. 
      
  - MAPI_DEFERRED_ERRORS: Ermöglicht **OpenMsgStore** die erfolgreiche Rückgabe, möglicherweise bevor der Nachrichtenspeicher für den aufrufenden Client vollständig verfügbar ist. Wenn der Nachrichtenspeicher nicht verfügbar ist, kann ein nachfolgender Objektaufruf einen Fehler auslösen. 
      
  - MDB \_ NO_DIALOG: Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Kennzeichen festgelegt ist und **OpenMsgStore** über unzureichende Konfigurationsinformationen verfügt, um den Nachrichtenspeicher ohne die Hilfe des Benutzers zu öffnen, wird MAPI_E_LOGON_FAILED zurückgegeben. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Nachrichtenspeicher erforderlich sind. 
      
  - MDB \_ NO_MAIL: Der Nachrichtenspeicher sollte nicht zum Senden oder Empfangen von E-Mails verwendet werden. Wenn dieses Kennzeichen festgelegt ist, benachrichtigt MAPI den MAPI-Spooler nicht, dass dieser Nachrichtenspeicher geöffnet wird.
      
  - MDB \_ ONLINE: Im Modus "Cached Exchange" kann ein Client oder Dienstanbieter diese Methode mit MDB_ONLINE aufrufen, um die Verbindung mit dem lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver zu öffnen. Sie können einen Exchange Speicher nicht gleichzeitig in derselben MAPI-Sitzung im Cachemodus und im nicht zwischengespeicherten Modus öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.
      
  - MDB_TEMPORARY: Weist die MAPI an, dass der Nachrichtenspeicher nicht permanent ist und nicht der Nachrichtenspeichertabelle hinzugefügt werden sollte. Dieses Flag wird verwendet, um sich beim Nachrichtenspeicher anzumelden, damit Informationen programmgesteuert aus dem Profilabschnitt abgerufen werden können. 
      
  - MDB_WRITE: Fordert Lese-/Schreibberechtigungen für den Nachrichtenspeicher an.
    
_lppMDB_
  
> [out] Zeiger auf einen Zeiger des Nachrichtenspeichers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Nachrichtenspeicher zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der durch  _lpEntryID_ angegebene Nachrichtenspeicher ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codepage des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicheranbieter verfügt über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter abzurufen. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::OpenMsgStore-Methode** öffnet einen bestimmten Nachrichtenspeicher. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt. Wenn Sie das flag MDB_WRITE festlegen, wird Ihnen möglicherweise noch keine Lese-/Schreibberechtigung gewährt. Die letzte Zugriffsebene, die MAPI dem Nachrichtenspeicher zuweist, hängt von Ihrer Berechtigungsstufe, dem Nachrichtenspeicher selbst und dem Nachrichtenspeicheranbieter ab. 
  
Wenn Sie **OpenMsgStore** aufrufen, um einen Nachrichtenspeicher mit schreibgeschützter Berechtigung zu öffnen, geschieht Folgendes: 
  
- Für die **\_ PR-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft des Stores sind die \_ STORE-MODIFY_OK und \_ store-CREATE_OK Bits nicht festgelegt. 
    
- Aufrufe zum Öffnen von Nachrichten oder Ordnern des Nachrichtenspeichers mithilfe von [IMAPISession::OpenEntry](imapisession-openentry.md) mit festgelegter MAPI_MODIFY Flag schlagen fehl. 
    
- Aufrufe zum Öffnen einer der Eigenschaften der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) mit dem flag MAPI_MODIFY schlagen fehl. 
    
- Aufrufe an eine der folgenden Methoden schlagen fehl: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Aufrufe der folgenden Methoden schlagen fehl, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, unabhängig davon, ob das Ziel mit dem Quellnachrichtenspeicher übereinstimmt oder ein anderer schreibgeschützter Speicher ist.
    
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

