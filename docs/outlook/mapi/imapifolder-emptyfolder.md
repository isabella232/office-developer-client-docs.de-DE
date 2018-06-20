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
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792122"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Betrifft**: Outlook 
  
Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst löschen.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Ordner geleert wird. Die folgenden Kennzeichen können festgelegt werden:
    
DEL_ASSOCIATED 
  
> Löscht alle Unterordner, einschließlich Unterordner, die Nachrichten mit zugeordneten Inhalt enthalten. Das Flag DEL_ASSOCIATED ist nur für Ordner der obersten Ebene, die, dem der Anruf auf fungiert.
    
DELETE_HARD_DELETE
  
> Entfernt alle Nachrichten, einschließlich vorläufig Gelöschte Objekte.
    
FOLDER_DIALOG 
  
> Eine Statusanzeige angezeigt, während der Vorgang fortgesetzt wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Ordner wurde erfolgreich geleert.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber der Ordner wurde nicht vollständig geleert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::EmptyFolder** -Methode löscht alle eines Ordners ohne den Ordner selbst löschen. 
  
Während eines Anrufs **EmptyFolder** werden gesendete Nachrichten nicht gelöscht. 
  
Zugehörige Inhalt eines Ordners enthalten Nachrichten, die Ansichten, Regeln, benutzerdefinierten Formularen und benutzerdefinierte im Lösungsspeicher beschreiben und können auch Formulardefinitionen enthalten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) -Methode nicht für Nachrichten in den Ordner, die gesendet wurden. Gesendete Nachrichten werden nicht gelöscht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**EmptyFolder** wurde erfolgreich den Ordner geleert.  <br/> |S_OK  <br/> |
|**EmptyFolder** konnte den Ordner zu leeren.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** konnte nicht abgeschlossen.  <br/> |Einen anderen Fehlerwert als  <br/> |
   
Wenn **EmptyFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. Möglicherweise wurden **EmptyFolder** können einige der Inhalt des Ordners löschen, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::EmptyFolder** -Methode, um den Inhalt des angegebenen Ordners zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

