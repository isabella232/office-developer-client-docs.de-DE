---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792100"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Betrifft**: Outlook 
  
Kopiert oder Verschiebt einen Unterordner.
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Unterordners kopieren oder verschieben.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden soll, dem auf der _LpDestFolder_ -Parameter verweist auf den Ordner zugreifen darstellt. Übergeben von NULL bewirkt, dass die Standardordner-Schnittstelle zurück, die den Dienstanbieter [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Gültige Werte für _LpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Ordner öffnen, um den Unterordner kopiert oder verschoben wird.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des Ordners kopiert oder verschoben in ihr neues Ziel. Wenn _LpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Unterordners Quelle für den Namen des Zielordners verwendet. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert. Die folgenden Kennzeichen können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner im Unterordner kopiert werden sollte auch kopiert werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der identifizierten _LpEntryID_ Unterordner kopiert. Mit einem Verschiebevorgang wird das Verhalten COPY_SUBFOLDERS standardmäßig unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige.
    
FOLDER_MOVE 
  
> Der Unterordner ist anstelle von verschoben werden kopiert. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.
    
MAPI_DECLINE_OK 
  
> Dem Nachricht Speicheranbieter informiert werden, dass wenn diese **CopyFolder** implementiert, durch die des Unterstützungsobjekts [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) oder [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufrufen, **CopyFolder** stattdessen sofort MAPI_E_ zurückgegeben werden soll DECLINE_COPY. 
    
PARAMETER MAPI_UNICODE 
  
> Der Name des Zielordners ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Nachrichtenanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und der Nachricht Speicher-Anbieter unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, die verschoben oder kopiert ist identisch mit der von einem Unterordner im Zielordner. Der Nachricht Speicheranbieter erfordert eindeutige Ordnernamen.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch den Aufruf einer Support, und der Aufrufer das Flag MAPI_DECLINE_OK verstrichen ist.
    
MAPI_E_FOLDER_CYCLE 
  
> Der Source-Ordner enthält direkt oder indirekt den Zielordner. Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit der Quell- und Zielserver Ordner teilweise geändert werden kann. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::CopyFolder** -Methode kopiert oder Verschiebt einen Unterordner von einem Speicherort an einen anderen. Der Unterordner kopiert oder verschoben wird in den Zielordner als Unterordner hinzugefügt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Beim Kopieren oder verschieben-Vorgang mehrere Ordner umfasst, wie durch Festlegen der COPY_SUBFOLDERS-Flag angegeben, führen Sie den Vorgang für jeden Ordner möglichst vollständig. In einigen Fällen einen der Ordner verschoben oder kopiert wurde ist nicht vorhanden oder bereits verschoben oder kopiert wurde an anderer Stelle. Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.
  
Versuchen Sie, die alle Nachricht-Eintragsbezeichner in der kopierten Nachrichten beibehalten werden. Sie sollten auch versuchen, Eintragsbezeichner beibehalten, aber es ist nicht erforderlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** wurde erfolgreich kopiert oder jede Nachricht und Unterordner verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte erfolgreich kopieren oder verschieben Sie jede Nachricht und Unterordner.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** konnte nicht abgeschlossen.  <br/> |Einen Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **CopyFolder** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. **CopyFolder** wurden möglicherweise kopieren oder verschieben Sie eine oder mehrere Nachrichten und Unterordner vor den Fehler auftreten können. 
  
Wenn ein Eintrag Bezeichner für einen Ordner, der nicht vorhanden ist _LpEntryID_übergeben wird, gibt **CopyFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, je nach den Nachrichtenspeicher Implementierung. 
  
Je nach Anbieter die Nachricht die Eintrags-ID der ursprünglichen Nachricht oder nicht in der kopierten Nachricht beibehalten werden. Sie sollten Eintragsbezeichner nach Möglichkeit beizubehalten, aber es ist nicht erforderlich. Sie können die folgenden Szenarien in der Regel abhängig:
  
- Wenn Sie einen Ordner zwischen zwei verschiedene Arten von Nachrichtenspeicher verschieben, wird die Eintrags-ID unbedingt ändern.
    
- Wenn Sie einen Ordner zwischen zwei Nachrichtenspeicher des gleichen Typs, ändert sich die Eintrags-ID fast immer.
    
- Wenn Sie einen Ordner an einen anderen Speicherort in der gleichen Nachrichtenspeicher verschieben, die Eintrags-ID kann oder möglicherweise nicht ändern, abhängig von der Nachricht Speicheranbieter.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::CopyFolder** -Methode, um Ordner von einem Speicherort in einen anderen zu kopieren. MFCMAPI (engl.) speichert Quellordners während des Kopiervorgangs und die Kopie tatsächlich während der Einfügevorgang ausführt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

