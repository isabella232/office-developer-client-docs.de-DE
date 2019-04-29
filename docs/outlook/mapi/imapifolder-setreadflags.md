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
  
Legt das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehrerer der Nachrichten des Ordners fest oder löscht das Senden von Lese Berichten. 
  
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
  
> in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die die Nachricht oder Nachrichten identifizieren, die Read Flags haben, um festzulegen oder zu löschen. Wenn _lpMsgList_ auf NULL festgelegt ist, werden die Lese Kennzeichen für alle Nachrichten des Ordners festgelegt oder deaktiviert. 
    
_ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
_lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.
    
_ulFlags_
  
> in Eine Bitmaske von Flags, die die Einstellung der Read-Kennzeichnung einer Nachricht und die Verarbeitung von Lese Berichten steuert. Die folgenden Flags können festgelegt werden:
    
  - CLEAR_READ_FLAG: das MSGFLAG_READ-flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein Lesebericht sollte nicht gesendet werden. 
        
  - CLEAR_NRN_PENDING: das MSGFLAG_NRN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein ungelesener Bericht sollte nicht gesendet werden. 
        
  - CLEAR_RN_PENDING: das MSGFLAG_RN_PENDING-Flag sollte in **PR_MESSAGE_FLAGS** gelöscht werden, und ein Lesebericht sollte nicht gesendet werden. 
        
  - GENERATE_RECEIPT_ONLY: ein Lesebericht sollte gesendet werden, wenn ein ausstehender ist, aber es sollte keine Änderung des Status des MSGFLAG_READ-Flags geben.
        
  - MAPI_DEFERRED_ERRORS: ermöglicht es **SetReadFlags** , erfolgreich zurückzugeben, möglicherweise bevor der Vorgang abgeschlossen wurde. 
        
  - MESSAGE_DIALOG: zeigt während des Vorgangs eine Statusanzeige an.
    
  - SUPPRESS_RECEIPT: ein ausstehender Lesebericht sollte abgebrochen werden, wenn ein Lesebericht angefordert wurde und dieser Aufruf den Status der Nachricht von ungelesen in lesen ändert. Wenn durch diesen Anruf der Status der Nachricht nicht geändert wird, kann der Nachrichtenspeicher Anbieter dieses Flag ignorieren.
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
> Die Read-Kennzeichnung für die angegebenen Nachrichten wurde erfolgreich festgelegt oder gelöscht.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachrichtenspeicher Anbieter unterstützt die Unterdrückung von Lese Berichten nicht.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden inkompatiblen Kombinationen von Flags wird im _ulFlags_ -Parameter festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Nachrichten wurden erfolgreich verarbeitet. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPIFolder:: SetReadFlags** -Methode wird das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft eines oder mehrerer der Nachrichten des Ordners festgelegt oder gelöscht. Durch Festlegen des MSGFLAG_READ-Flags wird eine Nachricht als gelesen markiert, was nicht unbedingt darauf hinweist, dass der vorgesehene Empfänger die Nachricht tatsächlich gelesen hat. 
  
**SetReadFlags** verwaltet auch das Senden von Lese Berichten. 
  
Die Read-Kennzeichnung kann für Folgendes nicht geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die an anderer Stelle verschoben wurden.
    
- Mit Lese-/Schreibzugriff geöffnete Nachrichten.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können sich entscheiden, das Senden von Lese Berichten und die Anforderung zur Unterdrückung von Lese Berichten nicht zu unterstützen. Um zu verhindern, dass ein Lesebericht unterdrückt wird, geben Sie MAPI_E_NO_SUPPRESS zurück, wenn **SetReadFlags** mit SUPPRESS_RECEIPT im _ulFlags_ -Parameter festgelegt wird. 
  
Wenn der Parameter _lpMsgList_ auf mehr als eine Nachricht zeigt, führen Sie den Vorgang für jede Nachricht so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher. 
  
Wenn keines der Flags im Parameter _ulFlags_ festgelegt wird, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie Sie sofort fest, und senden Sie ausstehende Lese Berichte, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist.
    
Wenn das SUPPRESS_RECEIPT-Flag festgelegt ist, gelten die folgenden Regeln:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, tun Sie nichts. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es fest und brechen alle ausstehenden Lese Berichte ab.
    
Wenn das CLEAR_READ_FLAG-Flag festgelegt ist, deaktivieren Sie das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** -Eigenschaft jeder Nachricht, und senden Sie keine Lese Berichte. 
  
Wenn das GENERATE_RECEIPT_ONLY-Flag festgelegt ist, senden Sie ausstehende Lese Berichte. MSGFLAG_READ nicht festlegen oder löschen.
  
Wenn sowohl die SUPPRESS_RECEIPT-als auch die GENERATE_RECEIPT_ONLY-Flags festgelegt sind, legen Sie **PR_READ_RECEIPT_REQUESTED** auf false fest, wenn es festgelegt ist, und senden Sie keinen Lesebericht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.  <br/> |S_OK  <br/> |
|**SetReadFlags** konnte jede Nachricht nicht erfolgreich verarbeiten.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **SetReadFlags** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **SetReadFlags** kann möglicherweise das MSGFLAG_READ-flag für eine oder mehrere der Nachrichten festlegen oder löschen, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI verwendet die **IMAPIFolder:: SetReadFlags** -Methode, um den Lesestatus für die angegebenen Nachrichten manuell festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)  
- [Kanonische Pidtagreadreceiptrequested (-Eigenschaft](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)  
- [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

