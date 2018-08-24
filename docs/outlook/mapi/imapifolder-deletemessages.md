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
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578633"
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
  
> [in] Ein Zeiger auf eine [ENTRYLIST](entrylist.md) -Struktur, die enthält die Anzahl der Nachrichten löschen und ein Array von [ENTRYID](entryid.md) -Strukturen, die die Nachrichten zu identifizieren. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichten gelöscht werden. Die folgenden Kennzeichen können festgelegt werden:
    
DELETE_HARD_DELETE
  
> Entfernt alle Nachrichten, einschließlich vorläufig Gelöschte Objekte.
    
MESSAGE_DIALOG 
  
> Eine Statusanzeige wird angezeigt, wie der-Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die angegebene Nachricht(en) wurden erfolgreich gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Nachrichten erfolgreich gelöscht wurden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::DeleteMessages** -Methode löscht Nachrichten aus einem Ordner. Nachrichten, die nicht vorhanden sind, an anderer Stelle verschoben wurden, die mit Lese-/Schreibzugriff geöffnet sind oder, die derzeit übermittelt hat, können nicht gelöscht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehr als eine Nachricht umfasst, führen Sie den Vorgang möglichst vollständig für jeden Ordner, auch wenn eine oder mehrere Nachrichten nicht gelöscht werden kann. Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|Jede Nachricht **DeleteMessages** wurde gelöscht.  <br/> |S_OK  <br/> |
|**DeleteMessages** konnte nicht erfolgreich jede Nachricht und Unterordner löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** konnte nicht abgeschlossen.  <br/> |Einen Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteMessages** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. Möglicherweise wurden **DeleteMessages** können eine oder mehrere Nachrichten löschen, bevor der Fehler auftritt. 
  
 **DeleteMessages** gibt MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach den Nachrichtenspeicher Implementierung zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI (engl.) wird die **IMAPIFolder::DeleteMessages** -Methode zum Löschen der angegebenen Nachrichten verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

