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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792118"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Betrifft**: Outlook 
  
Legt fest oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) von einem oder mehreren der Nachrichten, die den Ordner und das Senden von lesen Berichte verwaltet. 
  
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
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die identifizieren, die Nachricht oder Nachrichten, die Flags festzulegen oder zu deaktivieren, um gelesen haben. Wenn _LpMsgList_ auf NULL festgelegt ist, kennzeichnet das Lesen für alle, die Nachrichten aus den Ordnern festgelegt oder deaktiviert werden. 
    
_ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
_lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe des MAPI-Implementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.
    
_ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Einstellung des Volumens Flags eine Nachricht und die Verarbeitung steuert Lesen von Berichten. Die folgenden Kennzeichen können festgelegt werden:
    
  - CLEAR_READ_FLAG: Das Flag MSGFLAG_READ sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht lesen nicht gesendet werden soll. 
        
  - CLEAR_NRN_PENDING: Das Flag MSGFLAG_NRN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht ungelesener nicht gesendet werden soll. 
        
  - CLEAR_RN_PENDING: Das Flag MSGFLAG_RN_PENDING sollte in **PR_MESSAGE_FLAGS** deaktiviert werden und ein Bericht lesen nicht gesendet werden soll. 
        
  - GENERATE_RECEIPT_ONLY: Lese-Bericht gesendet werden soll, wenn eine steht noch aus, aber keine Änderung im Zustand des MSGFLAG_READ Flags werden soll.
        
  - MAPI_DEFERRED_ERRORS: Ermöglicht **SetReadFlags** erfolgreich, möglicherweise beendet, bevor der Vorgang abgeschlossen ist. 
        
  - MESSAGE_DIALOG: Eine Statusanzeige angezeigt, während der Vorgang fortgesetzt wird.
    
  - SUPPRESS_RECEIPT: Ein ausstehender lesen Bericht sollte abgebrochen werden, wenn ein Bericht lesen angefordert und dieses Anrufs den Status der Nachricht vom ungelesene zum Lesen von ändert. Wenn dieses Anrufs nicht den Status der Nachricht ändert, kann der Nachricht Speicheranbieter dieses Flag ignorieren.
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
> Das Lesen-Flag für die angegebene Nachricht(en) wurde erfolgreich festgelegt oder deaktiviert.
    
MAPI_E_NO_SUPPRESS 
  
> Der Nachricht Speicheranbieter unterstützt nicht die Unterdrückung der Lese-Berichte.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine der folgenden inkompatiblen Kombinationen von Flags wird in der _UlFlags_ -Parameter festgelegt: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, jedoch nicht alle Nachrichten erfolgreich verarbeitet wurden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::SetReadFlags** -Methode aktiviert oder deaktiviert das Flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** -Eigenschaft von einem oder mehreren der Nachrichten, die den Ordner. Markiert die Nachricht als gelesen, die nicht unbedingt darauf hinweist, dass der Empfänger die Nachricht tatsächlich gelesen hat das MSGFLAG_READ-Flag festlegen. 
  
**SetReadFlags** verwaltet auch das Senden von Berichten lesen. 
  
Das Flag lesen kann nicht für die folgenden geändert werden:
  
- Nachrichten, die nicht vorhanden sind.
    
- Nachrichten, die wurden verschoben eingehen.
    
- Nachrichten, die mit Lese-/Schreibzugriff geöffnet sind.
    
- Nachrichten, die derzeit übermittelt werden.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können nicht für das Senden von Lese-Berichten und die Anforderung an die schreibgeschützte Reports unterdrücken unterstützen. Zum Vermeiden von unterdrücken lesen-Bericht zurückgeben Sie MAPI_E_NO_SUPPRESS **SetReadFlags** mit SUPPRESS_RECEIPT festlegen in der _UlFlags_ -Parameter aufgerufen wird. 
  
Wenn der Parameter _LpMsgList_ auf mehr als eine Nachricht zeigt, führen Sie den Vorgang für jede Nachricht möglichst vollständig. Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird. 
  
Wenn keiner der Werte in der _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln: 
  
- Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt.
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es sofort und senden Sie alle ausstehenden lesen Berichte, wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist.
    
Wenn das Flag SUPPRESS_RECEIPT festgelegt ist, gelten die folgenden Regeln:
  
- Wenn MSGFLAG_READ bereits festgelegt ist, wird keine Aktion durchgeführt. 
    
- Wenn MSGFLAG_READ nicht festgelegt ist, legen Sie es und Abbrechen an alle ausstehenden lesen Berichte.
    
Wenn das Flag CLEAR_READ_FLAG festgelegt ist, deaktivieren Sie die Kennzeichen MSGFLAG_READ in jede Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft und senden Sie keine lesen Berichte. 
  
Wenn das Flag GENERATE_RECEIPT_ONLY festgelegt ist, senden Sie alle ausstehenden Lese-Berichte. Führen Sie MSGFLAG_READ nicht festgelegt oder löschen.
  
Wenn die SUPPRESS_RECEIPT und die GENERATE_RECEIPT_ONLY Flags festgelegt werden, **PR_READ_RECEIPT_REQUESTED** auf FALSE festgelegt, wenn sie festgelegt ist, und senden Sie einen read Bericht nicht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**SetReadFlags** hat jede Nachricht erfolgreich verarbeitet.  <br/> |S_OK  <br/> |
|**SetReadFlags** konnte nicht erfolgreich jede Nachricht zu verarbeiten.  <br/> |MAPI_W_PARTIAL_COMPLETION oder MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** konnte nicht abgeschlossen.  <br/> |Einen Fehlerwert außer MAPI_E_NOT_FOUND  <br/> |
   
Wenn **SetReadFlags** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. **SetReadFlags** wurden möglicherweise Lage festzulegen oder das Flag MSGFLAG_READ für eine oder mehrere Nachrichten zu löschen, bevor der Fehler auftritt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::SetReadFlags** -Methode, manuell gelesen-Status für die angegebenen Nachrichten festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)  
- [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

