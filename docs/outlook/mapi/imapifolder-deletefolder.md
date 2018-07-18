---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792093"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Betrifft**: Outlook 
  
Löscht einen Unterordner.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Unterordners zu löschen.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Löschen des Unterordners steuert. Die folgenden Kennzeichen können festgelegt werden:
    
DEL_FOLDERS 
  
> Alle Unterordner des Unterordners auf den _LpEntryID_ sollte gelöscht werden. 
    
DEL_MESSAGES 
  
> Alle Nachrichten in den Unterordner auf den _LpEntryID_ sollte gelöscht werden. 
    
FOLDER_DIALOG 
  
> Eine Statusanzeige sollte angezeigt werden, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich gelöscht.
    
MAPI_E_HAS_FOLDERS 
  
> Der zu löschende Unterordner enthält Unterordner, und das Flag DEL_FOLDERS wurde nicht festgelegt. Die Unterordner wurden nicht gelöscht.
    
MAPI_E_HAS_MESSAGES 
  
> Der zu löschende Unterordner enthält Nachrichten, und das Flag DEL_MESSAGES wurde nicht festgelegt. Der Unterordner wurde nicht gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge erfolgreich gelöscht wurden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::DeleteFolder** -Methode löscht einen Unterordner. In der Standardeinstellung **DeleteFolder** funktioniert nur bei leeren Ordnern, jedoch können Sie sie erfolgreich für nicht leeren Ordner durch zwei Werte festlegen: DEL_FOLDERS und DEL_MESSAGES. Nur leere Ordner oder die Ordner, in denen die DEL_FOLDERS und die DEL_MESSAGES Kennzeichen für den Aufruf **DeleteFolder** festlegen können gelöscht werden. DEL_FOLDERS können alle Unterordner des Ordners entfernt werden soll. DEL_MESSAGES können alle Nachrichten von den Ordner entfernt werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehrere Ordner umfasst, führen Sie den Vorgang für jeden Ordner möglichst vollständig. Manchmal einen der zu löschenden Ordner wurde ist nicht vorhanden oder verschoben oder kopiert wurde an anderer Stelle. Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|Jede Nachricht und Unterordner **DeleteFolder** wurde gelöscht.  <br/> |S_OK  <br/> |
|**DeleteFolder** konnte jede Nachricht und Unterordner erfolgreich zu löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** konnte nicht abgeschlossen.  <br/> |Einen Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. **DeleteFolder** wurden möglicherweise eine oder mehrere Nachrichten und Unterordner löschen, bevor der Fehler auftritt. 
  
Wenn eine oder mehrere Unterordner können nicht gelöscht werden, gibt **DeleteFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach der Implementierung der Nachricht Informationsdienst zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::DeleteFolder** -Methode zum Löschen von Ordnern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

