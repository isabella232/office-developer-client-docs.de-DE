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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420885"
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den übergeordneten Ordner des Ordners verwendet werden soll, der kopiert oder verschoben werden soll.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den übergeordneten Ordner des Ordners, der kopiert oder verschoben werden soll. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl in der Eintrags-ID, auf die _von lpEntryID verwiesen wird._
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Ordners, der kopiert oder verschoben werden soll. 
    
 _lpInterface_
  
> [in] Reserviert; muss NULL sein.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Ordner, der den zu kopierende oder zu verschiebende Ordner empfangen soll.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners; Andernfalls NULL, was angibt, dass der kopierte oder verschobene Ordner denselben Namen wie der Quellordner haben soll (der Ordner, auf den _lpEntryID verweist)._
    
 _ulUIParam_
  
> [in] Ein Handle des Fensters für das Dialogfeld Statusanzeige und zugehörige Fenster. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG ist in _ulFlags festgelegt._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner des Ordners sollten kopiert oder verschoben werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der durch  _lpEntryID identifizierte_ Ordner kopiert. Bei einem Verschiebevorgang ist COPY_SUBFOLDERS das Standardverhalten, unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige eines Statusindikators an.
    
FOLDER_MOVE 
  
> Der Ordner sollte verschoben werden, anstatt zu kopieren. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.
    
MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, hat der Name des Ordners das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Der Name des verschobenen oder kopierten Ordners ist identisch mit dem eines Unterordners im Zielordner. Der Nachrichtenspeicheranbieter erfordert, dass Ordnernamen eindeutig sind. Der Vorgang wird beendet, ohne abgeschlossen zu werden.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CopyFolder-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **IMAPISupport::CopyFolder** in ihrer Implementierung von [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) aufrufen, um einen einzelnen Ordner aus einem übergeordneten Ordner in einen anderen zu kopieren oder zu verschieben. 
  
 **IMAPISupport::CopyFolder** fügt den kopierten oder verschobenen Ordner als Unterordner des Zielordners hinzu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPISupport::CopyFolder** ermöglicht das gleichzeitige Umbenennen und Verschieben von Ordnern sowie das Kopieren oder Verschieben von Unterordnern des betroffenen Ordners. Um alle im kopierten oder verschobenen Ordner geschachtelten Unterordner zu kopieren oder zu verschieben, übergeben Sie das COPY_SUBFOLDERS in  _ulFlags_. 
  
Erwarten Sie die folgenden Rückgabewerte unter den folgenden Bedingungen:
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** hat den Ordner und alle unterordner erfolgreich kopiert oder verschoben, sofern zutreffend.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte nicht alle Ordner erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **CopyFolder** einen Fehlerwert zurückgibt, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. Ein oder mehrere Ordner hätten kopiert oder verschoben werden können, bevor **CopyFolder** den Fehler erlebte. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

