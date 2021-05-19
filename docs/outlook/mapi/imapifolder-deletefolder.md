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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des zu löschende Unterordners.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG ist in _ulFlags festgelegt._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Löschen des Unterordners steuert. Die folgenden Kennzeichen können festgelegt werden:
    
DEL_FOLDERS 
  
> Alle Unterordner des Unterordners, auf die  _von lpEntryID_ verwiesen wird, sollten gelöscht werden. 
    
DEL_MESSAGES 
  
> Alle Nachrichten im Unterordner, auf die  _von lpEntryID_ verwiesen wird, sollten gelöscht werden. 
    
FOLDER_DIALOG 
  
> Ein Statusindikator sollte angezeigt werden, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich gelöscht.
    
MAPI_E_HAS_FOLDERS 
  
> Der zu löschende Unterordner enthält Unterordner, und das DEL_FOLDERS wurde nicht festgelegt. Die Unterordner wurden nicht gelöscht.
    
MAPI_E_HAS_MESSAGES 
  
> Der zu löschende Unterordner enthält Nachrichten, und das DEL_MESSAGES wurde nicht festgelegt. Der Unterordner wurde nicht gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich gelöscht. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::D eleteFolder-Methode** löscht einen Unterordner. **DeleteFolder** wird standardmäßig nur für leere Ordner verwendet, Sie können es jedoch erfolgreich für nicht leere Ordner verwenden, indem Sie zwei Flags festlegen: DEL_FOLDERS und DEL_MESSAGES. Es können nur leere Ordner oder Ordner gelöscht werden, die die DEL_FOLDERS und DEL_MESSAGES für den **DeleteFolder-Aufruf** festlegen. DEL_FOLDERS ermöglicht das Entfernen aller Unterordner des Ordners. DEL_MESSAGES können alle Nachrichten des Ordners entfernt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehrere Ordner umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist einer der zu löschenden Ordner nicht vorhanden oder wurde an anderer Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**DeleteFolder** hat alle Nachrichten und Unterordner erfolgreich gelöscht.  <br/> |S_OK  <br/> |
|**DeleteFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. **DeleteFolder** konnte möglicherweise eine oder mehrere Nachrichten und Unterordner löschen, bevor der Fehler aufgetreten ist. 
  
Wenn ein oder mehrere Unterordner nicht gelöscht werden können, gibt **DeleteFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, abhängig von der Implementierung des Nachrichtenspeicheranbieters, zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFolder::D eleteFolder-Methode,** um Ordner zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

