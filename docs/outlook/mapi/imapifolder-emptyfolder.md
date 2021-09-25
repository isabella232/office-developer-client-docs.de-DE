---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a1e1440e6bc6e7cbf9015affa2cfc2f69f41a3f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596323"
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
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das FOLDER_DIALOG Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Ordner geleert wird. Die folgenden Flags können festgelegt werden:
    
DEL_ASSOCIATED 
  
> Löscht alle Unterordner, einschließlich Unterordnern, die Nachrichten mit zugeordneten Inhalten enthalten. Das flag DEL_ASSOCIATED hat nur für den Ordner auf oberster Ebene Bedeutung, auf dem der Aufruf ausgeführt wird.
    
DELETE_HARD_DELETE
  
> Entfernt alle Nachrichten, einschließlich vorläufig gelöschter Nachrichten, dauerhaft.
    
FOLDER_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich geleert.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber der Ordner wurde nicht vollständig geleert. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::EmptyFolder-Methode** löscht den gesamten Inhalt eines Ordners, ohne den Ordner selbst zu löschen. 
  
Während eines **EmptyFolder-Aufrufs** werden gesendete Nachrichten nicht gelöscht. 
  
Die zugeordneten Inhalte eines Ordners umfassen Nachrichten, die zum Beschreiben von Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefiniertem Lösungsspeicher verwendet werden, und können auch Formulardefinitionen enthalten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) nicht für Nachrichten in dem Ordner auf, die übermittelt wurden. Gesendete Nachrichten werden nicht gelöscht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**EmptyFolder** hat den Ordner erfolgreich geleert.  <br/> |S_OK  <br/> |
|**EmptyFolder** konnte den Ordner nicht vollständig leeren.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **EmptyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **EmptyFolder** konnte möglicherweise einen Teil des Ordnerinhalts löschen, bevor der Fehler auftritt. 
  
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

