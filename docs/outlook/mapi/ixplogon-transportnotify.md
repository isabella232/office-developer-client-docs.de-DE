---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5429f98a0335ae99b719d0f15b66a95ba87430e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792889"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Betrifft**: Outlook 
  
Signalisiert das Auftreten eines Ereignisses zu den der Transportdienst Benachrichtigung angefordert.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske aus Flags, die Benachrichtigungsereignisse signalisiert. Die folgenden Kennzeichen können festgelegt werden, durch die MAPI-Warteschlange bei der Eingabe und müssen bei der Ausgabe unverändert zurückgegeben werden:
    
NOTIFY_ABORT_DEFERRED 
  
> Benachrichtigt den Transportdienst, dass eine Nachricht für die sie Verantwortung anerkannt werden verzögert wird. Nur Transportanbieter, Verzögerungen unterstützen, müssen dieses Flag unterstützen. Der Parameter _LppvData_ verweist auf die Eintrags-ID der Nachricht wurde abgebrochen. Nachrichten, die die MAPI-Warteschlange, nicht verarbeitet wurden können weiterhin durch Aufrufen der Methode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) verzögert werden. 
    
NOTIFY_BEGIN_INBOUND 
  
> Die MAPI-Warteschlange kann jetzt eingehende Nachrichten für diesen Anbieter Transport akzeptieren. Die MAPI-Warteschlange ruft regelmäßig die [IXPLogon::Poll](ixplogon-poll.md) -Methode, wenn der Adressbuchhierarchie das Flag LOGON_SP_POLL mit dem Aufruf von [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) bei der Anmeldung festgelegt. Nachdem das Flag NOTIFY_BEGIN_INBOUND festgelegt ist, berücksichtigt die MAPI-Warteschlange das NOTIFY_NEWMAIL-Flag, das im Aufruf der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode übergeben. Die Status-Tabellenzeile für die Sitzung mit dem Transport sollte vor der Rückgabe durch Aufrufen der Methode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) aktualisiert werden. Die Flags NOTIFY_BEGIN_INBOUND und NOTIFY_END_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Signalisiert der Adressbuchhierarchie, um eingehende Nachrichten so schnell wie möglich zu durchlaufen. Um die Einhaltung dieser Benachrichtigung sollte der Adressbuchhierarchie STATUS_INBOUND_FLUSH Flag in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)), dessen Status Tabellenzeile festlegen, als er mithilfe von **ModifyStatusRow kann**. Ein eingehender messaging Zyklus ist abgeschlossen, wenn der Anbieter bestimmt, dass sie alle heruntergeladen hat, die er kann, oder sie einen Aufruf der **TransportNotify** -Methode mit dem Flag NOTIFY_END_INBOUND_FLUSH erhalten hat. Bis zum Ende des eingehenden messaging Zyklus sollte der Anbieter nicht die [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) -Methode aufrufen oder anderweitig abgeben Zyklen für das Betriebssystem, um die Geschwindigkeit Übermittlung eingehender Nachrichten. Dies ist akzeptabel, da die MAPI-Warteschlange in der Regel NOTIFY_BEGIN_INBOUND_FLUSH nur in der Antwort auf einen Benutzer an, über eine Clientanwendung verwendet, um alle Nachrichten jetzt übermitteln. Am Ende der eingehenden Schreibvorgang wurde sollte der Anbieter **SpoolerNotify** zum Deaktivieren Sie der Kennzeichen STATUS_INBOUND_FLUSH in der Statuszeile der **PR_STATUS_CODE** -Eigenschaft verwenden. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ausgehende Vorgänge können nun für diesen Anbieter Transport auftreten. Wenn vorhanden alle Nachrichten sind, die für diesen Anbieter gesendet werden, folgt ein Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode. Die Tabellenzeile Status für diese Sitzung sollten vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_BEGIN_OUTBOUND und NOTIFY_END_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Verhält sich das Flag NOTIFY_BEGIN_INBOUND_FLUSH, aber bezieht sich auf ausgehende Nachrichten. Das Flag des geeigneten Status ist STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Die MAPI-Warteschlange muss Weiterleiten der Nachricht kündigen, für die der _LppvData_ Parameter verweist auf den 32-Bit-Wert aus der **IXPLogon::SubmitMessage** -Methode aufrufen. Das Flag NOTIFY_CANCEL_MESSAGE kann festgelegt werden, ohne der Adressbuchhierarchie zurückgibt **SubmitMessage**, **IXPLogon::StartMessage**oder **IXPLogon::EndMessage** -Methode aufrufen, die die Nachricht zugeordnet ist. Der Transportdienst muss so bald wie möglich aus der Einstiegspunkt zurückgeben, die die Nachricht wurde abgebrochen behandelt. Für eine eingehende Nachricht, die zurzeit verarbeitet wird, sollte der Adressbuchhierarchie speichern die eingehende Nachricht, wo sie derzeit gespeichert ist und das Dokument zum nächsten geeigneten Zeitpunkt erneut übermitteln. Die Nachricht-Objektdaten, die bereits für die eingehende Nachricht gespeichert werden verworfen. Wenn der Adressbuchhierarchie keine dieser 32-Bit-Wert jederzeit **StartMessage** oder **SubmitMessage** aktualisiert wurden, ist der Wert 0 für ausgehende Nachrichten und 1 für eingehende Nachrichten. 
    
NOTIFY_END_INBOUND 
  
> Eingehende Vorgänge müssen für diesen Anbieter Transport diese erlöschen. Die MAPI-Warteschlange nicht mehr mit der **Umfrage** -Methode und NOTIFY_NEWMAIL für diese Sitzung ignoriert. In-Process-Nachrichten müssen abgeschlossen werden. Die Status-Tabellenzeile für die Sitzung Transport sollte durch Aufrufen von [ModifyStatusRow](imapisupport-modifystatusrow.md) vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Der Transportdienst aus dem eingehende flush-Modus betrachten benachrichtigt. Der Transportdienst sollten nicht beendet, herunterladen, aber herunterladen im Hintergrund ausgeführt werden soll. Die Status-Tabellenzeile für die Sitzung Transport sollte durch Aufrufen von **ModifyStatusRow** beim Einhalten der Adressbuchhierarchie dieser Benachrichtigung kann aktualisiert werden. 
    
NOTIFY_END_OUTBOUND 
  
> Ausgehende Vorgänge müssen für diesen Anbieter Transport diese erlöschen. Die MAPI-Warteschlange nicht mehr **SubmitMessage** aufrufen und ignoriert die **SpoolerNotify** NOTIFY_READYTOSEND-Flag. Wenn es eine ausgehende Nachricht gerade gesendet wird ist, nicht beendet werden soll. Verwenden Sie das NOTIFY_CANCEL_MESSAGE-Flag, um Übermittlung einer Nachricht zu beenden. Die Tabellenzeile Status für diese Sitzung sollte durch Aufrufen von **ModifyStatusRow** vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Works bezieht sich auf ähnliche Weise auf NOTIFY_END_INBOUND_FLUSH, aber auf ausgehende Nachrichten. Das Flag des geeigneten Status ist STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Ein Zeiger auf einen Zeiger auf Daten. Weitere Informationen dazu, welche _LppvData_ gibt an finden Sie in der Beschreibung für den Parameter _LpulFlags_ . 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange die **IXPLogon::TransportNotify** -Methode aufgerufen, um der Adressbuchhierarchie über Ereignisse signalisieren für die Benachrichtigung angefordert wurde. Diese Ereignisse enthalten eine MAPI-Warteschlange Anforderung zur Übertragung einer Nachricht, Anfang oder Ende eingehende oder ausgehende Transport-Vorgänge und Anfang oder Ende eines Vorgangs zum Löschen einer Warteschlange eingehende oder ausgehende Nachrichten Abbrechen. 
  
Wenn der Benutzer versucht, eine Nachricht abzubrechen, die zuvor der Adressbuchhierarchie zurückgestellt wurde, ruft die MAPI-Warteschlange **TransportNotify**, in dem NOTIFY_ABORT_DEFERRED und NOTIFY_CANCEL_MESSAGE-Flag in _UlFlags_übergeben. Wenn die MAPI-Warteschlange meldet sich ab und immer Nachrichten in der Warteschlange noch, übergibt sie nur NOTIFY_ABORT_DEFERRED in _UlFlags_ beim **TransportNotify**aufrufen.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Anbieter muss Zugriff auf seine Daten für dieses Anrufs synchronisieren, da die MAPI-Warteschlange diese Methode für ein anderes Fenster aus einem anderen Thread der Ausführung oder aus einer Prozedur aufrufen kann. Dies tritt wahrscheinlich auf, wenn die MAPI-Warteschlange den Abbruch einer Nachricht signalisiert, dass der Adressbuchhierarchie senden gestartet wurde.
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon: IUnknown](ixplogoniunknown.md)

