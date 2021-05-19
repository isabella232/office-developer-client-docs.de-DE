---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426072"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht eine oder mehrere Nachrichten.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMsgList_
  
> [in] Ein Zeiger auf eine [ENTRYLIST-Struktur,](entrylist.md) die die Anzahl der zu löschenden Nachrichten und ein Array von [ENTRYID-Strukturen](entryid.md) enthält, die die Nachrichten identifizieren. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichten gelöscht werden. Die folgenden Kennzeichen können festgelegt werden:
    
DELETE_HARD_DELETE
  
> Entfernt dauerhaft alle Nachrichten, einschließlich der gelöschten Nachrichten.
    
MESSAGE_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die angegebene Nachricht oder Nachrichten wurde erfolgreich gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Nachrichten wurden erfolgreich gelöscht. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::D eleteMessages-Methode** löscht Nachrichten aus einem Ordner. Nachrichten, die nicht vorhanden sind, an eine andere Stelle verschoben wurden, die mit Lese-/Schreibberechtigung geöffnet sind oder die derzeit übermittelt werden, können nicht gelöscht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehrere Nachrichten umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus, auch wenn eine oder mehrere Nachrichten nicht gelöscht werden können. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**DeleteMessages** hat jede Nachricht erfolgreich gelöscht.  <br/> |S_OK  <br/> |
|**DeleteMessages** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. **DeleteMessages** konnte möglicherweise eine oder mehrere der Nachrichten löschen, bevor der Fehler aufgetreten ist. 
  
 **DeleteMessages** gibt MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, abhängig von der Implementierung des Nachrichtenspeichers, zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFolder::D eleteMessages-Methode,** um die angegebenen Nachrichten zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

