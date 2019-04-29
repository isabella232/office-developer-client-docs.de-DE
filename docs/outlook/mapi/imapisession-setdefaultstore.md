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
  
> in Eine Bitmaske von Flags, die die Einstellung des Standardnachrichten Speichers steuert. Diese Flags schließen sich gegenseitig aus; nur eines der folgenden Flags kann festgelegt werden:
    
MAPI_DEFAULT_STORE
  
> Richtet den Nachrichtenspeicher als Sitzungs Standard ein. Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_DEFAULT_STORE-Flag in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Spalte festgelegt wird.
    
MAPI_PRIMARY_STORE
  
> Richtet den Nachrichtenspeicher als den bei der Anmeldung zu verwendenden Speicher ein. Wenn es sich bei dem Nachrichtenspeicher nicht um den Standardspeicher handelt, sollten Clients diesen standardmäßig festlegen. Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_PRIMARY_STORE-Flag in der **PR_RESOURCE_FLAGS** -Spalte festgelegt wird. 
    
MAPI_SECONDARY_STORE
  
> Richtet den Nachrichtenspeicher als den bei der Anmeldung zu verwendenden Speicher ein, wenn der primäre Nachrichtenspeicher nicht verfügbar ist. Wenn ein Client den primären Speicher nicht öffnen kann, sollte er den sekundären Speicher öffnen und als Standard festlegen. Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_SECONDARY_STORE-Flag in der **PR_RESOURCE_FLAGS** -Spalte festgelegt wird. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Legt das STATUS_SIMPLE_STORE-Flag in der **PR_RESOURCE_FLAGS** -Eigenschaft des Nachrichtenspeichers in der Zeile Status Tabelle, Nachrichtenspeicher-Tabellenzeile und im Sitzungsprofil fest. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Legt das STATUS_SIMPLE_STORE-Flag in der **PR_RESOURCE_FLAGS** -Eigenschaft des Nachrichtenspeichers in der Zeile Status Tabelle und Nachrichtenspeichertabelle fest. Das Profil wird nicht geändert. 
    
 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers, der als Standard verwendet werden soll. Wenn ein Client in _LPENTRYID_NULL übergibt, wird kein Nachrichtenspeicher als Standard ausgewählt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPISession:: SetDefaultStore** -Methode wird ein Nachrichtenspeicher als einer der folgenden festgelegt: 
  
- Der standardmäßige Nachrichtenspeicher für die Sitzung.
    
- Der primäre Nachrichtenspeicher für die Sitzung.
    
- Der sekundäre Nachrichtenspeicher für die Sitzung.
    
Zum Einrichten eines Nachrichtenspeichers als Standard muss für den Nachrichtenspeicher die folgenden Flags in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt sein:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können den standardmäßigen Nachrichtenspeicher für die Sitzung bestimmen, indem Sie die Statustabelle abrufen und nach der Einstellung des STATUS_DEFAULT_STORE-Flags in der **PR_RESOURCE_FLAGS** -Spalte suchen. Die Zeile mit dieser Einstellung stellt den Nachrichtenspeicher dar, der als Sitzungs Standard festgelegt ist. 
  
Wenn das MAPI_DEFAULT_STORE-oder das MAPI_SIMPLE_STORE_PERMANENT-Flag festgelegt ist, aktualisiert MAPI das Profil, die Nachrichtenspeichertabelle und die Statustabelle. 
  
Bei jeder Änderung der Standardeinstellung für den Nachrichtenspeicher werden die folgenden Benachrichtigungen generiert:
  
- Für jede betroffene Zeile in der Nachrichtenspeicher-und Statustabelle wird eine **fnevTableModified** -Ereignisbenachrichtigung ausgegeben. 
    
- Eine interne Benachrichtigung wird an den MAPI-Spooler ausgegeben. Vorgänge, die bereits ausgeführt werden, werden ohne Änderung abgeschlossen. neue Vorgänge, die den standardmäßigen Nachrichtenspeicher betreffen, wie das Herunterladen von Nachrichten, werden für den neuen Standardspeicher verarbeitet.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnSetDefaultStore  <br/> |MFCMAPI verwendet die **IMAPISession:: SetDefaultStore** -Methode, um den ausgewählten Speicher als Standardspeicher festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagresourceflags (-Eigenschaft](pidtagresourceflags-canonical-property.md)
  
[Kanonische PidTagStoreSupportMask-Eigenschaft](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

