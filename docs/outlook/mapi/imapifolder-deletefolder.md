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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417406"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu löschenden Unterordners.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Löschen des Unterordners steuert. Die folgenden Flags können festgelegt werden:
    
DEL_FOLDERS 
  
> Alle Unterordner des Unterordners, auf die durch _lpEntryID_ verwiesen wird, sollten gelöscht werden. 
    
DEL_MESSAGES 
  
> Alle Nachrichten im Unterordner, auf die von _lpEntryID_ verwiesen wird, sollten gelöscht werden. 
    
FOLDER_DIALOG 
  
> Während des Vorgangs wird eine Statusanzeige angezeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich gelöscht.
    
MAPI_E_HAS_FOLDERS 
  
> Der gelöschte Ordner enthält Unterordner, und das DEL_FOLDERS-Flag wurde nicht festgelegt. Die Unterordner wurden nicht gelöscht.
    
MAPI_E_HAS_MESSAGES 
  
> Der gelöschte Ordner enthält Nachrichten, und das DEL_MESSAGES-Flag wurde nicht festgelegt. Der Unterordner wurde nicht gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich gelöscht. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::D eletefolder** -Methode löscht einen Unterordner. Standardmäßig wird **DeleteFolder** nur in leeren Ordnern ausgeführt, aber Sie können es erfolgreich in nicht leeren Ordnern verwenden, indem Sie zwei Flags festlegen: DEL_FOLDERS und DEL_MESSAGES. Nur leere Ordner oder Ordner, die sowohl die DEL_FOLDERS-als auch die DEL_MESSAGES-Flags für den **DeleteFolder** -Aufruf festlegen, können gelöscht werden. DEL_FOLDERS ermöglicht das Entfernen aller Unterordner des Ordners; DEL_MESSAGES ermöglicht das Entfernen aller Nachrichten des Ordners. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehr als einen Ordner umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist einer der zu löschenden Ordner nicht vorhanden oder wurde an anderer Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**DeleteFolder** hat alle Nachrichten und Unterordner erfolgreich gelöscht.  <br/> |S_OK  <br/> |
|**DeleteFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **DeleteFolder** kann möglicherweise eine oder mehrere der Nachrichten und Unterordner gelöscht haben, bevor der Fehler auftritt. 
  
Wenn ein oder mehrere Unterordner nicht gelöscht werden können, gibt **DELETEFOLDER** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück, je nach der Implementierung des Nachrichtenspeicher Anbieters. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFolder::D eletefolder** -Methode, um Ordner zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

