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
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280178"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt einen Unterordner.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu Kopier-oder verschobenen Unterordners.
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, auf den der _lpDestFolder_ -Parameter zeigt. Das übergeben von NULL bewirkt, dass der Dienstanbieter die Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)zurückgibt. Gültige Werte für _lpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> in Ein Zeiger auf den geöffneten Ordner, um den kopierten oder verschobenen Unterordner zu empfangen.
    
 _lpszNewFolderName_
  
> in Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners in seinem neuen Ziel. Wenn _lpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Quell-Unterordners für den Namen des Zielordners verwendet. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag im _ulFlags_ -Parameter ist festgelegt. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner des zu kopierenden Unterordners sollten ebenfalls kopiert werden. Wenn COPY_SUBFOLDERS nicht für einen Kopiervorgang festgelegt ist, wird nur der durch _lpEntryID_ angegebene Unterordner kopiert. Bei einem Verschiebungsvorgang ist das COPY_SUBFOLDERS-Verhalten die Standardeinstellung, unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
FOLDER_MOVE 
  
> Der Unterordner soll statt kopiert werden. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicher Anbieter, dass bei der Implementierung von **CopyFolder** durch Aufrufen des [IMAPISupport::D ocopyto](imapisupport-docopyto.md) oder [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) -Methode CopyFolder stattdessen sofort **** MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Der Name des Zielordners ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Ordnername im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Nachrichtenspeicher Anbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Nachrichtenspeicher Anbieter unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, der verschoben oder kopiert wird, entspricht dem eines Unterordners im Zielordner. Der Nachrichtenspeicher Anbieter benötigt eindeutige Ordnernamen.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Support Objektmethode, und der Aufrufer hat das MAPI_DECLINE_OK-Flag übergeben.
    
MAPI_E_FOLDER_CYCLE 
  
> Der Quellordner enthält direkt oder indirekt den Zielordner. Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass der Quell-und der Zielordner teilweise geändert werden können. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: CopyFolder** -Methode kopiert oder verschiebt einen Unterordner von einem Speicherort an einen anderen. Der Unterordner, der kopiert oder verschoben wird, wird dem Zielordner als Unterordner hinzugefügt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Kopier-oder Verschiebungsvorgang mehr als einen Ordner umfasst, wie durch Festlegen des COPY_SUBFOLDERS-Flags angegeben, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist der Ordner, der verschoben oder kopiert werden soll, nicht vorhanden oder wurde bereits an anderer Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.
  
Versuchen Sie, alle Nachrichteneingabe-IDs in den kopierten Nachrichten beizubehalten. Sie sollten auch versuchen, Eintrags-IDs beizubehalten, aber es ist nicht erforderlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**Rückgabewert**|
|:-----|:-----|
|**CopyFolder** hat alle Nachrichten und Unterordner erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte alle Nachrichten und Unterordner nicht erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **CopyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **CopyFolder** kann möglicherweise eine oder mehrere der Nachrichten und Unterordner kopiert oder verschoben haben, bevor der Fehler auftritt. 
  
Wenn ein Eintragsbezeichner für einen Ordner, der nicht vorhanden ist, in _lpEntryID_übergeben wird, gibt **COPYFOLDER** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück, je nach der Implementierung des Nachrichtenspeichers. 
  
Je nach Nachrichtenspeicher Anbieter kann die Eintrags-ID der ursprünglichen Nachricht in der kopierten Nachricht beibehalten werden. Sie sollten Eintrags-IDs nach Möglichkeit beibehalten, aber es ist nicht erforderlich. Sie können in der Regel von den folgenden Szenarien abhängen:
  
- Wenn Sie einen Ordner zwischen zwei verschiedenen Nachrichtenspeicher Typen verschieben, wird der Eintragsbezeichner sicher geändert.
    
- Wenn Sie einen Ordner zwischen zwei Nachrichtenspeicher des gleichen Typs verschieben, ändert sich die Eintrags-ID fast immer.
    
- Wenn Sie einen Ordner an einen anderen Speicherort im gleichen Nachrichtenspeicher verschieben, kann sich die Eintrags-ID je nach Nachrichtenspeicher Anbieter ändern.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnPasteFolder  <br/> |MFCMAPI verwendet die **IMAPIFolder:: CopyFolder** -Methode, um Ordner von einem Speicherort an einen anderen zu kopieren. MFCMAPI merkt sich während des Kopiervorgangs den Quellordner und führt die Kopie tatsächlich während des Einfügevorgangs aus.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

