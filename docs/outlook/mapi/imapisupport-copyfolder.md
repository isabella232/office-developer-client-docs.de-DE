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
ms.openlocfilehash: 0b079b311a68459a43b0a7659ddfbe94d96d7f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792344"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Betrifft**: Outlook 
  
Kopiert oder Verschiebt einen Ordner von seinem aktuellen übergeordneten Ordner in einer anderen übergeordneten Ordner.
  
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
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle des übergeordneten Ordners des Ordners kopiert oder verschoben werden Zugriff auf verwendet werden soll.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den übergeordneten Ordner des Ordners, kopiert oder verschoben werden soll. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf _LpEntryID_zeigt.
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Ordners, kopiert oder verschoben werden soll. 
    
 _lpInterface_
  
> [in] Reserviert. NULL muss sein.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Ordner, der den Empfangsordner kopiert oder verschoben werden soll.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des Ordners kopiert oder verschoben werden soll andernfalls NULL, die angibt, dass der Ordner kopierte oder verschobene als Quellordners (in den Ordner auf den _LpEntryID_) den gleichen Namen verfügen soll.
    
 _ulUIParam_
  
> [in] Ein Handle für das Fenster für das Dialogfeld Symbol Status und zugehörige Fenster. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag FOLDER_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner des Ordners sollte kopiert oder verschoben werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der Ordner, die vom _LpEntryID_ kopiert. Mit einem Verschiebevorgang wird das Verhalten COPY_SUBFOLDERS standardmäßig unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige.
    
FOLDER_MOVE 
  
> Der Ordner verschoben werden soll anstelle von kopiert. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.
    
PARAMETER MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, die verschoben oder kopiert ist identisch mit der von einem Unterordner im Zielordner. Der Nachricht Speicheranbieter erfordert, dass Ordnernamen eindeutig sein. Der Vorgang wird beendet, ohne abzuschließen.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CopyFolder** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht-Anbieter können in ihrer Durchführung des [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) zu kopieren oder verschieben ein einzelnes Ordners aus einem übergeordneten Ordner in einen anderen **IMAPISupport::CopyFolder** aufrufen. 
  
 **IMAPISupport::CopyFolder** fügt den kopierte oder verschobenen Ordner als Unterordner des Zielordners. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPISupport::CopyFolder** ermöglicht das gleichzeitige umbenennen und Verschieben von Ordnern und das Kopieren oder Verschieben von Unterordner des betroffenen. Zum Kopieren oder verschieben alle Unterordner im Ordner kopiert oder verschoben geschachtelt, übergeben Sie die Kennzeichen COPY_SUBFOLDERS _UlFlags_. 
  
Davon ausgehen Sie, dass die folgenden Rückgabewerte in den folgenden Situationen:
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** erfolgreich kopieren oder verschieben den Ordner und alle Unterordner ein, falls zutreffend.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte erfolgreich kopieren oder verschieben Sie alle Ordner.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** konnte nicht abgeschlossen.  <br/> |Einen anderen Fehlerwert als  <br/> |
   
Wenn **CopyFolder** einen Fehlerwert zurückgibt, fahren Sie unter der Voraussetzung, die keine Arbeit ausgeführt wurde. Einen oder mehrere Ordner konnte kopiert oder verschoben wurden vor dem **CopyFolder** den Fehler aufgetreten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

