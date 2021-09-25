---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac2fb6c0ad29e16967b00425d9ca82cd3c52c8c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584374"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt einen Ordner aus seinem aktuellen übergeordneten Ordner in einen anderen übergeordneten Ordner.
  
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
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den übergeordneten Ordner des zu kopierenden oder zu verschiebenden Ordners verwendet werden soll.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den übergeordneten Ordner des Ordners, der kopiert oder verschoben werden soll. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den  _lpEntryID_ verweist.
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Ordners, der kopiert oder verschoben werden soll. 
    
 _lpInterface_
  
> [in] Reserviert; muss NULL sein.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Ordner, der den zu kopierenden oder zu verschiebenden Ordner empfangen soll.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners; andernfalls NULL, was angibt, dass der kopierte oder verschobene Ordner denselben Namen wie der Quellordner haben soll (der Ordner, auf den  _lpEntryID_ verweist).
    
 _ulUIParam_
  
> [in] Ein Handle des Fensters für das Dialogfeld "Statusanzeige" und die zugehörigen Fenster. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag FOLDER_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner des Ordners sollten kopiert oder verschoben werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der durch  _lpEntryID_ identifizierte Ordner kopiert. Bei einem Verschiebungsvorgang ist das COPY_SUBFOLDERS-Verhalten die Standardeinstellung, unabhängig davon, ob das Kennzeichen festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
FOLDER_MOVE 
  
> Der Ordner sollte verschoben werden, anstatt kopiert zu werden. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Ordner kopiert.
    
MAPI_UNICODE 
  
> Der Name des Ordners hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat der Name des Ordners das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, der verschoben oder kopiert wird, entspricht dem Namen eines Unterordners im Zielordner. Der Nachrichtenspeicheranbieter erfordert, dass Ordnernamen eindeutig sind. Der Vorgang wird ohne Abschluss beendet.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::CopyFolder-Methode** wird für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **IMAPISupport::CopyFolder** in ihrer Implementierung von [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) aufrufen, um einen einzelnen Ordner von einem übergeordneten Ordner in einen anderen zu kopieren oder zu verschieben. 
  
 **IMAPISupport::CopyFolder** fügt den kopierten oder verschobenen Ordner als Unterordner des Zielordners hinzu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **IMAPISupport::CopyFolder** ermöglicht das gleichzeitige Umbenennen und Verschieben von Ordnern sowie das Kopieren oder Verschieben von Unterordnern des betroffenen Ordners. Um alle im kopierten oder verschobenen Ordner geschachtelten Unterordner zu kopieren oder zu verschieben, übergeben Sie das flag COPY_SUBFOLDERS in _ulFlags._ 
  
Erwarten Sie die folgenden Rückgabewerte unter den folgenden Bedingungen:
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** hat den Ordner und ggf. alle zugehörigen Unterordner erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte nicht erfolgreich alle Ordner kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **CopyFolder** einen Fehlerwert zurückgibt, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. Ein oder mehrere Ordner könnten kopiert oder verschoben worden sein, bevor **CopyFolder** den Fehler festgestellt hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

