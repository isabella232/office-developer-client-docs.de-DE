---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 65c9727a2af44a939263342dfca01ac7b9c128ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630824"
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu kopierenden oder zu verschiebenden Unterordners.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, auf den der  _parameter lpDestFolder_ zeigt. Wenn NULL übergeben wird, gibt der Dienstanbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)zurück. Gültige Werte für  _lpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den geöffneten Ordner, um den kopierten oder verschobenen Unterordner zu erhalten.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners am neuen Ziel. Wenn  _lpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Quellunterordners für den Namen des Zielordners verwendet. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG-Flag im  _ulFlags-Parameter_ ist festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag FOLDER_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner im zu kopierenden Unterordner sollten ebenfalls kopiert werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der von  _lpEntryID_ identifizierte Unterordner kopiert. Bei einem Verschiebungsvorgang ist das COPY_SUBFOLDERS-Verhalten die Standardeinstellung, unabhängig davon, ob das Kennzeichen festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
FOLDER_MOVE 
  
> Der Unterordner soll verschoben werden, anstatt kopiert zu werden. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicheranbieter, dass **CopyFolder** stattdessen sofort MAPI_E_DECLINE_COPY zurückgeben sollte, wenn er **CopyFolder** durch Aufrufen der [IMAPISupport::D oCopyTo-](imapisupport-docopyto.md) oder [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) des Supportobjekts implementiert. 
    
MAPI_UNICODE 
  
> Der Name des Zielordners hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat der Ordnername das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das flag MAPI_UNICODE festgelegt, und der Nachrichtenspeicheranbieter unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Nachrichtenspeicheranbieter unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Der Name des Ordners, der verschoben oder kopiert wird, entspricht dem Namen eines Unterordners im Zielordner. Der Nachrichtenspeicheranbieter erfordert eindeutige Ordnernamen.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Supportobjektmethode, und der Aufrufer hat das flag MAPI_DECLINE_OK übergeben.
    
MAPI_E_FOLDER_CYCLE 
  
> Der Quellordner enthält den Zielordner direkt oder indirekt. Bevor diese Bedingung erkannt wurde, wurde möglicherweise umfangreiche Arbeit ausgeführt, sodass der Quell- und Zielordner teilweise geändert werden kann. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::CopyFolder-Methode** kopiert oder verschiebt einen Unterordner von einem Speicherort an einen anderen. Der zu kopierende oder verschobene Unterordner wird dem Zielordner als Unterordner hinzugefügt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Kopier- oder Verschiebungsvorgang mehrere Ordner umfasst, wie durch Festlegen des COPY_SUBFOLDERS Flags angegeben, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist einer der zu verschiebenden oder zu kopierenden Ordner nicht vorhanden oder wurde bereits an eine andere Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihrer Kontrolle liegt, z. B. zu wenig Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
Versuchen Sie, alle Nachrichteneingabe-IDs in den kopierten Nachrichten beizubehalten. Sie sollten auch versuchen, Eintragsbezeichner beizubehalten, dies ist jedoch nicht erforderlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** hat jede Nachricht und jeden Unterordner erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Ein beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **CopyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **CopyFolder** konnte möglicherweise eine oder mehrere Nachrichten und Unterordner kopieren oder verschieben, bevor der Fehler auftritt. 
  
Wenn ein Eintragsbezeichner für einen Ordner, der nicht vorhanden ist, in  _lpEntryID_ übergeben wird, **gibt CopyFolder** abhängig von der Implementierung des Nachrichtenspeichers MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND zurück. 
  
Abhängig vom Nachrichtenspeicheranbieter kann der Eintragsbezeichner der ursprünglichen Nachricht in der kopierten Nachricht beibehalten werden. Sie sollten Eintragsbezeichner nach Möglichkeit beibehalten, dies ist jedoch keine Anforderung. Sie können sich in der Regel auf die folgenden Szenarien verlassen:
  
- Wenn Sie einen Ordner zwischen zwei verschiedenen Arten von Nachrichtenspeichern verschieben, ändert sich der Eintragsbezeichner garantiert.
    
- Wenn Sie einen Ordner zwischen zwei Nachrichtenspeichern desselben Typs verschieben, ändert sich der Eintragsbezeichner fast immer.
    
- Wenn Sie einen Ordner an einen anderen Speicherort im selben Nachrichtenspeicher verschieben, ändert sich der Eintragsbezeichner je nach Nachrichtenspeicheranbieter möglicherweise oder nicht.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI verwendet die **IMAPIFolder::CopyFolder-Methode,** um Ordner von einem Speicherort an einen anderen zu kopieren. MFCMAPI speichert den Quellordner während des Kopiervorgangs und führt die Kopie tatsächlich während des Einfügevorgangs aus.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

