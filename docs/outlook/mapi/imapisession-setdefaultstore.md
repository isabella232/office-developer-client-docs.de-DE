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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e3c4125bf4fcf1881a0cba9b04a8bb6aa71f527d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792323"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Betrifft**: Outlook 
  
Stellt einen Nachrichtenspeicher als Standard-Informationsspeicher für die Sitzung her.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Einstellung der Standard-Informationsspeicher steuert. Diese Flags schließen sich gegenseitig aus; Es kann nur eine der folgenden Werte festgelegt werden:
    
MAPI_DEFAULT_STORE
  
> Stellt den Nachrichtenspeicher unverändert Sitzung her. Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_DEFAULT_STORE in der Spalte **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.
    
MAPI_PRIMARY_STORE
  
> Richtet den Nachrichtenspeicher als Speicher, die bei der Anmeldung verwendet werden. Wenn der Nachrichtenspeicher nicht des Standard-Informationsspeichers ist, sollte Clients die Standardeinstellung ermöglichen. Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_PRIMARY_STORE in der Spalte **PR_RESOURCE_FLAGS** festgelegt. 
    
MAPI_SECONDARY_STORE
  
> Richtet den Nachrichtenspeicher als Speicher bei der Anmeldung verwendet werden, wenn der primäre Nachrichtenspeicher nicht verfügbar ist. Wenn ein Client den primären Speicher nicht öffnen kann, sollten sie den sekundären Speicher öffnen und als Standard festlegen. Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_SECONDARY_STORE in der Spalte **PR_RESOURCE_FLAGS** festgelegt. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Das Flag STATUS_SIMPLE_STORE festgelegt in den Nachrichtenspeicher **PR_RESOURCE_FLAGS** -Eigenschaft in dessen Status Tabellenzeile Nachricht Store Tabellenzeile, und das Sitzungsprofil. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Legt das Flag STATUS_SIMPLE_STORE in den Nachrichtenspeicher **PR_RESOURCE_FLAGS** -Eigenschaft in den Status Tabellenzeile und Nachricht Store Tabellenzeile fest. Das Profil wird nicht geändert. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers, das als Standard vorgesehen ist. Wenn ein Client NULL _LpEntryID_übergibt, wird keine Nachrichtenspeicher als Standard ausgewählt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::SetDefaultStore** -Methode legt einen Nachrichtenspeicher als eine der folgenden: 
  
- Die Standard-Nachrichtenspeicher für die Sitzung.
    
- Die primäre Nachrichtenspeicher für die Sitzung.
    
- Die sekundäre Nachrichtenspeicher für die Sitzung.
    
Zum Einrichten eines Nachrichtenspeichers als Standard muss der Nachrichtenspeicher folgender Flags in seiner **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festlegen können:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können Standard-Informationsspeicher für die Sitzung bestimmen, indem Status abrufen und für die Einstellung des STATUS_DEFAULT_STORE-Flags in der Spalte **PR_RESOURCE_FLAGS** suchen. Die Zeile, die diese Einstellung hat stellt den Nachrichtenspeicher, der als Sitzung Standardproxy festgelegt ist. 
  
Wenn die MAPI_DEFAULT_STORE oder das MAPI_SIMPLE_STORE_PERMANENT-Flag festgelegt ist, aktualisiert MAPI Profil, Nachricht Store Tabelle und Statustabelle. 
  
Wenn die Nachricht Store Standardeinstellung eine Änderung vorgenommen wird, werden die folgenden Benachrichtigungen generiert:
  
- Für jede betroffene Zeile in der Nachricht Store und den Status der Tabelle wird eine Benachrichtigung bei **FnevTableModified** ausgegeben. 
    
- Eine interne Benachrichtigung wird an die Warteschlange MAPI ausgegeben. Bereits in Bearbeitung befindlichen Vorgänge werden ohne Änderung ausgefüllt. neue Vorgänge mit Standard-Informationsspeicher, wie etwa Nachricht herunterladen, werden für den neuen Standardspeicher verarbeitet.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::SetDefaultStore** -Methode, um der ausgewählten Speicher als Standard-Informationsspeicher festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagResourceFlags-Eigenschaft](pidtagresourceflags-canonical-property.md)
  
[Kanonische PidTagStoreSupportMask-Eigenschaft](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

