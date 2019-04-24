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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280106"
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
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Ordner geleert wird. Die folgenden Flags können festgelegt werden:
    
DEL_ASSOCIATED 
  
> Löscht alle Unterordner, einschließlich der Unterordner, die Nachrichten mit dem dazugehörigen Inhalt enthalten. Das DEL_ASSOCIATED-Flag hat nur für den Ordner auf oberster Ebene eine Bedeutung, für den der Anruf fungiert.
    
DELETE_HARD_DELETE
  
> Entfernt alle Nachrichten, einschließlich der gelöschten, dauerhaft.
    
FOLDER_DIALOG 
  
> Zeigt während des Vorgangs eine Statusanzeige an.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich geleert.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber der Ordner wurde nicht vollständig geleert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPIFolder:: EmptyFolder** -Methode werden alle Inhalte eines Ordners gelöscht, ohne dass der Ordner selbst gelöscht wird. 
  
Während eines **EmptyFolder** -Aufrufs werden übermittelte Nachrichten nicht gelöscht. 
  
Zu den zugeordneten Inhalten eines Ordners gehören Nachrichten, die zum Beschreiben von Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefiniertem Lösungsspeicher verwendet werden, und können auch Formulardefinitionen enthalten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) -Methode nicht für Nachrichten im Ordner auf, die übermittelt wurden. ÜberMittelte Nachrichten werden nicht gelöscht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**Rückgabewert**|
|:-----|:-----|
|**EmptyFolder** hat den Ordner erfolgreich geleert.  <br/> |S_OK  <br/> |
|**EmptyFolder** konnte den Ordner nicht vollständig leeren.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **EmptyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **EmptyFolder** kann möglicherweise einige Inhalte des Ordners löschen, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnEmptyFolder  <br/> |MFCMAPI verwendet die **IMAPIFolder:: EmptyFolder** -Methode, um den Inhalt des angegebenen Ordners zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

