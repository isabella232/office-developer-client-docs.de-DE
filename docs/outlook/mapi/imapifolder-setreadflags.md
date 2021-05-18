---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406913"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehreren Nachrichten des Ordners fest oder entfernt es und verwaltet das Senden von Leseberichten. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_lpMsgList_
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die Nachricht oder Nachrichten identifizieren, deren Lesekennzeichen festgelegt oder löschen werden sollen. Wenn  _lpMsgList_ auf NULL festgelegt ist, werden die Leseflags für alle Nachrichten des Ordners festgelegt oder geräumt. 
    
_ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
_lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der IMPLEMENTIERUNG von MAPI eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Einstellung des Lesekennzeichens einer Nachricht und die Verarbeitung von Leseberichten steuert. Die folgenden Kennzeichen können festgelegt werden:
    
  - CLEAR_READ_FLAG: Das MSGFLAG_READ sollte **in** der PR_MESSAGE_FLAGS und ein Lesebericht nicht gesendet werden. 
        
  - CLEAR_NRN_PENDING: Das MSGFLAG_NRN_PENDING-Flag sollte **in** der PR_MESSAGE_FLAGS und kein ungelesener Bericht gesendet werden. 
        
  - CLEAR_RN_PENDING: Das MSGFLAG_RN_PENDING sollte **in** der PR_MESSAGE_FLAGS und ein Lesebericht nicht gesendet werden. 
        
  - GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn ein Ausstehend ist, aber es sollte keine Änderung im Status des MSGFLAG_READ werden.
        
  - MAPI_DEFERRED_ERRORS: Ermöglicht die erfolgreiche Rückgabe von **SetReadFlags,** möglicherweise vor Abschluss des Vorgangs. 
        
  - MESSAGE_DIALOG: Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
  - SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen zu lesen ändert. Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
> Das Leseflag für die angegebene Nachricht oder Nachrichten wurde erfolgreich festgelegt oder geräumt.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden inkompatiblen Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Nachrichten wurden erfolgreich verarbeitet. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Mit **der IMAPIFolder::SetReadFlags-Methode** wird das MSGFLAG_READ-Flag in der **PR_MESSAGE_FLAGS-Eigenschaft** einer oder mehreren Nachrichten des Ordners festgelegt oder entfernt. Das Festlegen MSGFLAG_READ markiert eine Nachricht als gelesen, was nicht unbedingt darauf hinweist, dass der beabsichtigte Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Leseberichten. 
  
Das Leseflag kann für Folgendes nicht geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an anderer Stelle verschoben wurden.
    
- Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können entscheiden, das Senden von Leseberichten und die Anforderung zum Unterdrücken von Leseberichten nicht zu unterstützen. Um das Unterdrücken eines Leseberichts zu vermeiden, geben Sie MAPI_E_NO_SUPPRESS zurück, wenn **SetReadFlags** mit SUPPRESS_RECEIPT  _ulFlags-Parameter aufgerufen_ wird. 
  
Wenn der  _lpMsgList-Parameter_ auf mehrere Nachrichten zeigt, führen Sie den Vorgang für jede Nachricht so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher. 
  
Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es sofort fest, und senden Sie alle ausstehenden Leseberichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft festgelegt ist.
    
Wenn das SUPPRESS_RECEIPT festgelegt ist, gelten die folgenden Regeln:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie sie fest, und brechen Sie alle ausstehenden Leseberichte ab.
    
Wenn das CLEAR_READ_FLAG festgelegt ist, löschen Sie das MSGFLAG_READ in der  PR_MESSAGE_FLAGS-Eigenschaft jeder Nachricht, und senden Sie keine Leseberichte. 
  
Wenn das GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte. Legen Sie keine MSGFLAG_READ.
  
Wenn sowohl die SUPPRESS_RECEIPT als auch GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie **PR_READ_RECEIPT_REQUESTED** auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie keinen Lesebericht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.  <br/> |S_OK  <br/> |
|**SetReadFlags** konnte nicht jede Nachricht erfolgreich verarbeiten.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **SetReadFlags** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit durchgeführt wurde. **SetReadFlags** konnte möglicherweise das MSGFLAG_READ für eine oder mehrere Nachrichten festlegen oder löschen, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMAPIFolder::SetReadFlags-Methode,** um den Lesestatus für die angegebenen Nachrichten manuell fest.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)  
- [Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

