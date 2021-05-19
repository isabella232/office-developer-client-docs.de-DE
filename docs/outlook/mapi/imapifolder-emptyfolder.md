---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416783"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst zu löschen.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Ordner geleert wird. Die folgenden Kennzeichen können festgelegt werden:
    
DEL_ASSOCIATED 
  
> Löscht alle Unterordner, einschließlich Unterordner, die Nachrichten mit zugeordneten Inhalten enthalten. Das DEL_ASSOCIATED hat nur eine Bedeutung für den Ordner auf oberster Ebene, auf dem der Anruf funktioniert.
    
DELETE_HARD_DELETE
  
> Entfernt dauerhaft alle Nachrichten, einschließlich der gelöschten Nachrichten.
    
FOLDER_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich geleert.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, der Ordner wurde jedoch nicht vollständig geleert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::EmptyFolder-Methode** löscht alle Inhalte eines Ordners, ohne den Ordner selbst zu löschen. 
  
Während eines **EmptyFolder-Anrufs** werden übermittelte Nachrichten nicht gelöscht. 
  
Zu den zugeordneten Inhalten eines Ordners gehören Nachrichten, die zum Beschreiben von Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefiniertem Lösungsspeicher verwendet werden, und können auch Formulardefinitionen enthalten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) nicht für Nachrichten im Ordner auf, die übermittelt wurden. Übermittelte Nachrichten werden nicht gelöscht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**EmptyFolder** hat den Ordner erfolgreich geleert.  <br/> |S_OK  <br/> |
|**EmptyFolder** konnte den Ordner nicht vollständig leeren.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **EmptyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. **EmptyFolder** konnte möglicherweise einige Inhalte des Ordners löschen, bevor der Fehler aufgetreten ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI verwendet die **IMAPIFolder::EmptyFolder-Methode,** um den Inhalt des angegebenen Ordners zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

