---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341027"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt einen Ordner aus dem aktuellen übergeordneten Ordner in einen anderen übergeordneten Ordner.
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

 _lpSrcInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den übergeordneten Ordner des Ordners verwendet werden soll, der kopiert oder verschoben werden soll.
    
 _lpSrcFolder_
  
> in Ein Zeiger auf den übergeordneten Ordner des Ordners, der kopiert oder verschoben werden soll. 
    
 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die von _lpEntryID_verwiesen wird.
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Ordners, der kopiert oder verschoben werden soll. 
    
 _lpInterface_
  
> in Reserviert muss NULL sein.
    
 _lpDestFolder_
  
> in Ein Zeiger auf den Ordner, der den zu kopierenden oder zu verschiebenden Ordner erhalten soll.
    
 _lpszNewFolderName_
  
> in Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners; andernfalls NULL, wodurch angegeben wird, dass der kopierte oder verschobene Ordner den gleichen Namen wie der Quellordner haben soll (der Ordner, auf den von _lpEntryID_verwiesen wird).
    
 _ulUIParam_
  
> in Ein Handle des Fensters für das Dialogfeld Statusanzeige und zugehörige Fenster. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Kopier-oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner des Ordners sollten kopiert oder verschoben werden. Wenn COPY_SUBFOLDERS nicht für einen Kopiervorgang festgelegt ist, wird nur der durch _lpEntryID_ identifizierte Ordner kopiert. Bei einem Verschiebungsvorgang ist das COPY_SUBFOLDERS-Verhalten die Standardeinstellung, unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
FOLDER_MOVE 
  
> Der Ordner sollte verschoben und nicht kopiert werden. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.
    
MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, der verschoben oder kopiert wird, entspricht dem eines Unterordners im Zielordner. Der Nachrichtenspeicher Anbieter erfordert, dass Ordnernamen eindeutig sind. Der Vorgang wird angehalten, ohne abgeschlossen zu sein.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: CopyFolder** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter können **IMAPISupport:: CopyFolder** in ihrer Implementierung von [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) aufrufen, um einen einzelnen Ordner aus einem übergeordneten Ordner in einen anderen zu kopieren oder zu verschieben. 
  
 **IMAPISupport:: CopyFolder** fügt den kopierten oder verschobenen Ordner als Unterordner des Zielordners hinzu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPISupport:: CopyFolder** ermöglicht das gleichzeitige umbenennen und bewegen von Ordnern und das Kopieren oder bewegen von Unterordnern des betroffenen Ordners. Um alle im kopierten oder verschobenen Ordner geschachtelten Unterordner zu kopieren oder zu verschieben, müssen Sie das COPY_SUBFOLDERS-Flag in _ulFlags_. 
  
Erwarten Sie unter den folgenden Bedingungen die folgenden Rückgabewerte:
  
|**Bedingung**|**Rückgabewert**|
|:-----|:-----|
|**CopyFolder** hat den Ordner und alle zugehörigen Unterordner erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte nicht alle Ordner erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **CopyFolder** einen Fehlerwert zurückgibt, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. Ein oder mehrere Ordner konnten kopiert oder verschoben worden sein, bevor der **CopyFolder** auftritt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

