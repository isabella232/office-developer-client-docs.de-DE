---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426107"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Richtet einen Nachrichtenspeicher als Standardnachrichtenspeicher für die Sitzung ein.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Einstellung des Standardnachrichtenspeichers steuert. Diese Kennzeichen schließen sich gegenseitig aus. Es kann nur eines der folgenden Kennzeichen festgelegt werden:
    
MAPI_DEFAULT_STORE
  
> Richtet den Nachrichtenspeicher als Sitzungs standardwert ein. Aktualisiert die Statustabelle des Nachrichtenspeichers, indem STATUS_DEFAULT_STORE in der Spalte **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festlegen.
    
MAPI_PRIMARY_STORE
  
> Richtet den Nachrichtenspeicher als speicher ein, der bei der Anmeldung verwendet werden soll. Wenn der Nachrichtenspeicher nicht der Standardspeicher ist, sollten Clients ihn als Standard festlegen. Aktualisiert die Statustabelle des Nachrichtenspeichers, indem das STATUS_PRIMARY_STORE in der Spalte **PR_RESOURCE_FLAGS** wird. 
    
MAPI_SECONDARY_STORE
  
> Richtet den Nachrichtenspeicher als Speicher ein, der bei der Anmeldung verwendet werden soll, wenn der primäre Nachrichtenspeicher nicht verfügbar ist. Wenn ein Client den primären Speicher nicht öffnen kann, sollte er den sekundären Speicher öffnen und als Standard festlegen. Aktualisiert die Statustabelle des Nachrichtenspeichers, indem STATUS_SECONDARY_STORE in der Spalte **PR_RESOURCE_FLAGS** wird. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Legt das STATUS_SIMPLE_STORE in der **PR_RESOURCE_FLAGS-Eigenschaft** des Nachrichtenspeichers in der Statustabelle, der Tabellenzeile des Nachrichtenspeichers und im Sitzungsprofil fest. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Legt das STATUS_SIMPLE_STORE in der PR_RESOURCE_FLAGS-Eigenschaft des Nachrichtenspeichers in der Zeile "Statustabelle" und "Nachrichtenspeichertabelle" fest.  Das Profil wird nicht geändert. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Nachrichtenspeichers, der als Standard vorgesehen ist. Wenn ein Client NULL in  _lpEntryID übergibt,_ wird kein Nachrichtenspeicher als Standard ausgewählt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::SetDefaultStore-Methode** richtet einen Nachrichtenspeicher als einen der folgenden Methoden ein: 
  
- Der Standardnachrichtenspeicher für die Sitzung.
    
- Der primäre Nachrichtenspeicher für die Sitzung.
    
- Der sekundäre Nachrichtenspeicher für die Sitzung.
    
Um einen Nachrichtenspeicher als Standard einrichten zu können, muss der Nachrichtenspeicher die folgenden Flags in seiner **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft festgelegt haben:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können den Standardnachrichtenspeicher für die Sitzung ermitteln, indem Sie die Statustabelle abrufen und nach der Einstellung des STATUS_DEFAULT_STORE in der Spalte **PR_RESOURCE_FLAGS** suchen. Die Zeile mit dieser Einstellung stellt den Nachrichtenspeicher dar, der als Sitzungs standardwert festgelegt ist. 
  
Wenn entweder das MAPI_DEFAULT_STORE oder das MAPI_SIMPLE_STORE_PERMANENT festgelegt ist, aktualisiert MAPI das Profil, die Nachrichtenspeichertabelle und die Statustabelle. 
  
Wenn eine Änderung an der Standardeinstellung für den Nachrichtenspeicher vorgenommen wird, werden die folgenden Benachrichtigungen generiert:
  
- Für jede betroffene Zeile im Nachrichtenspeicher und in der Statustabelle wird eine **fnevTableModified-Ereignisbenachrichtigung** ausgegeben. 
    
- Eine interne Benachrichtigung wird an den MAPI-Spooler ausgegeben. Vorgänge, die bereits ausgeführt werden, werden ohne Änderung abgeschlossen. Neue Vorgänge, die den Standardnachrichtenspeicher betreffen, z. B. das Herunterladen von Nachrichten, werden für den neuen Standardspeicher verarbeitet.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI verwendet die **IMAPISession::SetDefaultStore-Methode,** um den ausgewählten Speicher als Standardspeicher zu festlegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PidTagResourceFlags (kanonische Eigenschaft)](pidtagresourceflags-canonical-property.md)
  
[PidTagStoreSupportMask (kanonische Eigenschaft)](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

