---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2f2066ec582b02f92cc17586bdecc7411d847987
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580006"
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
  
> [in] Ein Zeiger auf eine [ENTRYLIST-Struktur,](entrylist.md) die die Anzahl der zu löschenden Nachrichten enthält, und ein Array von [ENTRYID-Strukturen,](entryid.md) die die Nachrichten identifizieren. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das MESSAGE_DIALOG Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichten gelöscht werden. Die folgenden Flags können festgelegt werden:
    
DELETE_HARD_DELETE
  
> Entfernt alle Nachrichten, einschließlich vorläufig gelöschter Nachrichten, dauerhaft.
    
MESSAGE_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die angegebene Nachricht oder Die angegebenen Nachrichten wurden erfolgreich gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Nachrichten wurden erfolgreich gelöscht. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::D eleteMessages-Methode** löscht Nachrichten aus einem Ordner. Nachrichten, die nicht vorhanden sind, an eine andere Stelle verschoben wurden, die mit Lese-/Schreibberechtigung geöffnet sind oder derzeit übermittelt werden, können nicht gelöscht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehrere Nachrichten umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus, auch wenn eine oder mehrere der Nachrichten nicht gelöscht werden können. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihrer Kontrolle liegt, z. B. zu wenig Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**DeleteMessages** hat jede Nachricht erfolgreich gelöscht.  <br/> |S_OK  <br/> |
|**DeleteMessages** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** konnte nicht abgeschlossen werden.  <br/> |Ein beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **DeleteMessages** konnte möglicherweise eine oder mehrere der Nachrichten löschen, bevor der Fehler auftritt. 
  
 **DeleteMessages** gibt abhängig von der Implementierung des Nachrichtenspeichers MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück. 
  
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

