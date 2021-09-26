---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 69eaaf4e2f4997af48013760e843c56a044c435e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610608"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das MSGFLAG_READ Flag in der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) einer oder mehrerer Nachrichten des Ordners fest oder löscht es und verwaltet das Senden von Leseberichten. 
  
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
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die Nachricht oder Nachrichten identifizieren, deren Lesekennzeichen festgelegt oder gelöscht werden sollen. Wenn  _lpMsgList_ auf NULL festgelegt ist, werden die Leseflags für alle Nachrichten des Ordners festgelegt oder gelöscht. 
    
_ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
_lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Implementierung eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MESSAGE_DIALOG in  _ulFlags_ festgelegt ist.
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Einstellung des Lesekennzeichens einer Nachricht und die Verarbeitung von Leseberichten steuert. Die folgenden Flags können festgelegt werden:
    
  - CLEAR_READ_FLAG: Das flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
        
  - CLEAR_NRN_PENDING: Das flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein ungelesener Bericht gesendet werden. 
        
  - CLEAR_RN_PENDING: Das flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und es sollte kein Lesebericht gesendet werden. 
        
  - GENERATE_RECEIPT_ONLY: Ein Lesebericht sollte gesendet werden, wenn einer aussteht, der Status des MSGFLAG_READ-Flags sollte jedoch nicht geändert werden.
        
  - MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlags** die erfolgreiche Rückgabe, möglicherweise bevor der Vorgang abgeschlossen wurde. 
        
  - MESSAGE_DIALOG: Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
  - SUPPRESS_RECEIPT: Ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von "Ungelesen" in "Gelesen" ändert. Wenn dieser Aufruf den Status der Nachricht nicht ändert, kann der Nachrichtenspeicheranbieter dieses Kennzeichen ignorieren.
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
> Das Lesezeichen für die angegebene Nachricht bzw. die angegebenen Nachrichten wurde erfolgreich festgelegt oder gelöscht.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicheranbieter unterstützt die Unterdrückung von Leseberichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden inkompatiblen Kombinationen von Flags wird im  _ulFlags-Parameter_ festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Nachrichten wurden erfolgreich verarbeitet. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::SetReadFlags-Methode** legt das MSGFLAG_READ Flag in der **PR_MESSAGE_FLAGS** Eigenschaft einer oder mehrerer Nachrichten des Ordners fest oder löscht es. Durch Festlegen der MSGFLAG_READ Kennzeichnung wird eine Nachricht als gelesen gekennzeichnet, was nicht notwendigerweise bedeutet, dass der beabsichtigte Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Leseberichten. 
  
Das Lesezeichen kann für Folgendes nicht geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an eine andere Stelle verschoben wurden.
    
- Nachrichten, die mit Lese-/Schreibberechtigung geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können das Senden von Leseberichten und die Anforderung zum Unterdrücken von Leseberichten nicht unterstützen. Um das Unterdrücken eines Leseberichts zu vermeiden, geben Sie MAPI_E_NO_SUPPRESS zurück, wenn **SetReadFlags** mit SUPPRESS_RECEIPT im  _ulFlags-Parameter_ festgelegt wird. 
  
Wenn der  _parameter lpMsgList_ auf mehr als eine Nachricht zeigt, führen Sie den Vorgang für jede Nachricht so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihrer Kontrolle liegt, z. B. zu wenig Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher. 
  
Wenn keines der Flags im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, führen Sie nichts aus.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es sofort fest, und senden Sie alle ausstehenden Leseberichte, wenn die **eigenschaft PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.
    
Wenn das SUPPRESS_RECEIPT-Flag festgelegt ist, gelten die folgenden Regeln:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, führen Sie nichts aus. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest, und brechen Sie alle ausstehenden Leseberichte ab.
    
Wenn das flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie das MSGFLAG_READ Flag in der **eigenschaft PR_MESSAGE_FLAGS** jeder Nachricht, und senden Sie keine Leseberichte. 
  
Wenn das flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Leseberichte. MSGFLAG_READ nicht festlegen oder löschen.
  
Wenn die Flags SUPPRESS_RECEIPT und GENERATE_RECEIPT_ONLY festgelegt sind, legen Sie **PR_READ_RECEIPT_REQUESTED** auf FALSE fest, wenn sie festgelegt ist, und senden Sie keinen Lesebericht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.  <br/> |S_OK  <br/> |
|**SetReadFlags** konnte nicht alle Nachrichten erfolgreich verarbeiten.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** konnte nicht abgeschlossen werden.  <br/> |Ein beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **SetReadFlags** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. Möglicherweise konnte **SetReadFlags** das MSGFLAG_READ Flag für eine oder mehrere der Meldungen festlegen oder deaktivieren, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMAPIFolder::SetReadFlags-Methode,** um den Lesestatus für die angegebenen Nachrichten manuell festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)  
- [Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

