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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425659"
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
  
> [in] Ein Zeiger auf die Eintrags-ID des Zu kopieren oder zu verschiebende Unterordners.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, auf den der  _lpDestFolder-Parameter_ verweist. Durch Übergeben von NULL gibt der Dienstanbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer zurück.](imapifolderimapicontainer.md) Gültige Werte für  _lpInterface_ sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den geöffneten Ordner, um den kopierten oder verschobenen Unterordner zu empfangen.
    
 _lpszNewFolderName_
  
> [in] Ein Zeiger auf den Namen des kopierten oder verschobenen Ordners im neuen Ziel. Wenn  _lpszNewFolderName_ auf NULL festgelegt ist, wird der Name des Quellunterordners für den Namen des Zielordners verwendet. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG im  _ulFlags-Parameter_ ist festgelegt. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, das FOLDER_DIALOG ist in _ulFlags festgelegt._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert. Die folgenden Kennzeichen können festgelegt werden:
    
COPY_SUBFOLDERS 
  
> Alle Unterordner im zu kopierenden Unterordner sollten ebenfalls kopiert werden. Wenn COPY_SUBFOLDERS für einen Kopiervorgang nicht festgelegt ist, wird nur der durch  _lpEntryID_ identifizierte Unterordner kopiert. Bei einem Verschiebevorgang ist COPY_SUBFOLDERS das Standardverhalten, unabhängig davon, ob das Flag festgelegt ist. 
    
FOLDER_DIALOG 
  
> Fordert die Anzeige eines Statusindikators an.
    
FOLDER_MOVE 
  
> Der Unterordner soll verschoben und nicht kopiert werden. Wenn FOLDER_MOVE nicht festgelegt ist, wird der Unterordner kopiert.
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicheranbieter, dass **CopyFolder,** wenn er **CopyFolder** implementiert, indem die [IMAPISupport::D oCopyTo-](imapisupport-docopyto.md) oder [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) des Supportobjekts aufruft, stattdessen sofort MAPI_E_DECLINE_COPY. 
    
MAPI_UNICODE 
  
> Der Name des Zielordners ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Ordnername im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Ordner wurde erfolgreich kopiert oder verschoben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Nachrichtenspeicheranbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Nachrichtenspeicheranbieter unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Der Name des verschobenen oder kopierten Ordners ist identisch mit dem eines Unterordners im Zielordner. Der Nachrichtenspeicheranbieter benötigt eindeutige Ordnernamen.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Supportobjektmethode, und der Aufrufer hat das MAPI_DECLINE_OK übergeben.
    
MAPI_E_FOLDER_CYCLE 
  
> Der Quellordner enthält den Zielordner direkt oder indirekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass der Quell- und Zielordner teilweise geändert werden kann. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CopyFolder-Methode** kopiert oder verschiebt einen Unterordner von einem Speicherort an einen anderen. Der zu kopierende oder verschobene Unterordner wird dem Zielordner als Unterordner hinzugefügt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Kopier- oder Verschiebevorgang mehrere Ordner umfasst, wie durch Festlegen des COPY_SUBFOLDERS angegeben, führen Sie den Vorgang für jeden Ordner so vollständig wie möglich aus. Manchmal ist einer der zu verschiebenden oder zu kopierenden Ordner nicht vorhanden oder wurde bereits an anderer Stelle verschoben oder kopiert. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
Versuchen Sie, alle Nachrichteneintragsbezeichner in den kopierten Nachrichten zu behalten. Sie sollten auch versuchen, die Eintragsbezeichner zu erhalten, dies ist jedoch nicht erforderlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**CopyFolder** hat alle Nachrichten und Unterordner erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**CopyFolder** konnte nicht alle Nachrichten und Unterordner erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **CopyFolder** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. **CopyFolder** konnte möglicherweise eine oder mehrere Nachrichten und Unterordner kopieren oder verschieben, bevor der Fehler aufgetreten ist. 
  
Wenn eine Eintrags-ID für einen ordner, der nicht vorhanden ist, in  _lpEntryID_ übergeben wird, gibt **CopyFolder** MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND, abhängig von der Implementierung des Nachrichtenspeichers. 
  
Abhängig vom Nachrichtenspeicheranbieter kann der Eintragsbezeichner der ursprünglichen Nachricht in der kopierten Nachricht beibehalten werden. Sie sollten nach Möglichkeit Eintragsbezeichner beibehalten, aber es ist keine Anforderung. Sie können im Allgemeinen von den folgenden Szenarien abhängig sein:
  
- Wenn Sie einen Ordner zwischen zwei verschiedenen Typen von Nachrichtenspeichern verschieben, wird die Eintrags-ID garantiert geändert.
    
- Wenn Sie einen Ordner zwischen zwei Nachrichtenspeichern desselben Typs verschieben, ändert sich der Eintragsbezeichner fast immer.
    
- Wenn Sie einen Ordner an einen anderen Speicherort im gleichen Nachrichtenspeicher verschieben, kann sich der Eintragsbezeichner je nach Anbieter des Nachrichtenspeichers ändern.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI verwendet die **IMAPIFolder::CopyFolder-Methode,** um Ordner von einem Speicherort an einen anderen zu kopieren. MFCMAPI erinnert sich während des Kopiervorgangs an den Quellordner und führt die Kopie tatsächlich während des Einfügevorgangs aus.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

