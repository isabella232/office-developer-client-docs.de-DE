---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 25ec5dec5a614a94e4410eaec21e7d28ed513cd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576030"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu löschenden Unterordners.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag FOLDER_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Löschen des Unterordners steuert. Die folgenden Flags können festgelegt werden:
    
DEL_FOLDERS 
  
> Alle Unterordner des Unterordners, auf den  _lpEntryID_ verweist, sollten gelöscht werden. 
    
DEL_MESSAGES 
  
> Alle Nachrichten im Unterordner, auf die von  _lpEntryID_ verwiesen wird, sollten gelöscht werden. 
    
FOLDER_DIALOG 
  
> Während des Vorgangs sollte eine Statusanzeige angezeigt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich gelöscht.
    
MAPI_E_HAS_FOLDERS 
  
> Der zu löschende Unterordner enthält Unterordner, und das Flag DEL_FOLDERS wurde nicht festgelegt. Die Unterordner wurden nicht gelöscht.
    
MAPI_E_HAS_MESSAGES 
  
> Der zu löschende Unterordner enthält Nachrichten, und das DEL_MESSAGES Flag wurde nicht festgelegt. Der Unterordner wurde nicht gelöscht.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich gelöscht. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::D eleteFolder-Methode** löscht einen Unterordner. **DeleteFolder** arbeitet standardmäßig nur für leere Ordner, sie kann jedoch erfolgreich für nicht leere Ordner verwendet werden, indem Sie zwei Flags festlegen: DEL_FOLDERS und DEL_MESSAGES. Nur leere Ordner oder Ordner, die die Flags DEL_FOLDERS und DEL_MESSAGES für den **DeleteFolder-Aufruf** festlegen, können gelöscht werden. DEL_FOLDERS ermöglicht das Entfernen aller Unterordner des Ordners. DEL_MESSAGES können alle Nachrichten des Ordners entfernt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Löschvorgang mehrere Ordner umfasst, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist einer der zu löschenden Ordner nicht vorhanden oder wurde an eine andere Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihrer Kontrolle liegt, z. B. zu wenig Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**DeleteFolder** hat alle Nachrichten und Unterordner erfolgreich gelöscht.  <br/> |S_OK  <br/> |
|**DeleteFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich löschen.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** konnte nicht abgeschlossen werden.  <br/> |Ein beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **DeleteFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **DeleteFolder** konnte möglicherweise eine oder mehrere der Nachrichten und Unterordner löschen, bevor der Fehler auftritt. 
  
Wenn mindestens ein Unterordner nicht gelöscht werden kann, gibt **DeleteFolder** abhängig von der Implementierung des Nachrichtenspeicheranbieters MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFolder::D eleteFolder-Methode,** um Ordner zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

