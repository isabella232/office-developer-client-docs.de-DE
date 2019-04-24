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
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325767"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore](imsgstoreimapiprop.md) -Zeiger für den weiteren Zugriff zurück. 
  
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
  
> in Ein Handle für das übergeordnete Fenster des Dialogfelds "allgemeine Adresse" und andere zugehörige anzeigen.
    
_cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
_lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Nachrichtenspeichers. Der _lpEntryID_ -Parameter darf nicht NULL sein. 
    
_lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Nachrichtenspeicher verwendet werden soll. Übergeben von NULL bewirkt, dass der Parameter _lppMDB_ einen Zeiger auf die Standardschnittstelle für einen Nachrichtenspeicher (**IMsgStore**) zurückgibt.
    
_ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
  - MAPI_BEST_ACCESS: fordert, dass der Nachrichtenspeicher mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und den maximalen Client Anwendungsberechtigungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte der Nachrichtenspeicher mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte der Nachrichtenspeicher mit Leseberechtigung geöffnet werden. 
      
  - MAPI_DEFERRED_ERRORS: ermöglicht es **OpenMsgStore** , erfolgreich zurückzugeben, möglicherweise, bevor der Nachrichtenspeicher für den aufrufenden Client vollständig verfügbar ist. Wenn der Nachrichtenspeicher nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden. 
      
  - MDB\_-NO_DIALOG: verhindert die Anzeige von Anmelde Dialogfeldern. Wenn dieses Flag festgelegt ist und **OpenMsgStore** nicht über genügend Konfigurationsinformationen zum Öffnen des Nachrichtenspeichers ohne die Hilfe des Benutzers verfügt, wird MAPI_E_LOGON_FAILED zurückgegeben. Wenn dieses Flag nicht festgelegt ist, kann der Nachrichtenspeicher Anbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Nachrichtenspeicher erforderlich sind. 
      
  - MDB\_-NO_MAIL: der Nachrichtenspeicher sollte nicht zum Senden oder empfangen von e-Mails verwendet werden. Wenn dieses Flag festgelegt ist, wird die MAPI-Spooler nicht benachrichtigt, dass dieser Nachrichtenspeicher geöffnet wird.
      
  - MDB\_online: im Exchange-Cache-Modus kann ein Client oder Dienstanbieter diese Methode mit MDB_ONLINE aufrufen, um die Verbindung mit dem lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver zu öffnen. Sie können einen Exchange-Speicher nicht im Cache-Modus und gleichzeitig im nicht-Cache-Modus in derselben MAPI-Sitzung öffnen. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.
      
  - MDB_TEMPORARY: gibt MAPI an, dass der Nachrichtenspeicher nicht permanent ist und nicht der Nachrichtenspeichertabelle hinzugefügt werden sollte. Dieses Flag wird verwendet, um sich beim Nachrichtenspeicher anzumelden, damit Informationen programmgesteuert aus dem Abschnitt profile abgerufen werden können. 
      
  - MDB_WRITE: fordert Lese-/Schreibzugriff für den Nachrichtenspeicher an.
    
_lppMDB_
  
> Out Zeiger auf einen Zeiger des Nachrichtenspeichers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Nachrichtenspeicher zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der von _lpEntryID_ angegebene Nachrichtenspeicher ist nicht vorhanden. 
    
MAPI_E_UNKNOWN_CPID 
  
> Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.
    
MAPI_E_UNKNOWN_LCID 
  
> Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicher Anbieter hat Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Rufen Sie die [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) -Methode auf, um die Fehlerinformationen vom Anbieter abzurufen. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPISession:: OpenMsgStore** -Methode wird ein bestimmter Nachrichtenspeicher geöffnet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Standardberechtigungsstufe für Nachrichtenspeicher ist schreibgeschützt. Wenn Sie das MDB_WRITE-Flag festlegen, werden Ihnen möglicherweise weiterhin keine Lese-/Schreibzugriff erteilt. Die letzte Zugriffsebene, die MAPI dem Nachrichtenspeicher zuweist, hängt von Ihrer Berechtigungsstufe, dem Nachrichtenspeicher selbst und dem Nachrichtenspeicher Anbieter ab. 
  
Wenn Sie **OpenMsgStore** aufrufen, um einen Nachrichtenspeicher mit Schreibschutz Berechtigung zu öffnen, wird Folgendes ausgeführt: 
  
- Die **PR\_-STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Stores hat nicht\_die Speicher MODIFY_OK\_und speichert CREATE_OK-Bits festgelegt. 
    
- Aufrufe zum Öffnen eines der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPISession:: OpenEntry](imapisession-openentry.md) mit dem MAPI_MODIFY-Flagsatz schlagen fehl. 
    
- Aufrufe zum Öffnen einer der Eigenschaften der Nachrichten oder Ordner des Nachrichtenspeichers mithilfe von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) mit dem MAPI_MODIFY-Flag schlagen fehl. 
    
- Bei Aufrufen einer der folgenden Methoden tritt ein Fehler auf: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Bei Aufrufen der folgenden Methoden tritt ein Fehler auf, wenn das Ziel für die kopierte Nachricht schreibgeschützt ist, unabhängig davon, ob das Ziel mit dem Quell Nachrichtenspeicher identisch ist oder wenn es sich um einen anderen schreibgeschützten Speicher handelt.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI verwendet die **IMAPISession:: OpenMsgStore** -Methode, um einen Nachrichtenspeicher zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
- [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

