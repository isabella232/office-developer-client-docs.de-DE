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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428858"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Signalisiert das Auftreten eines Ereignisses, über das der Transportanbieter eine Benachrichtigung angefordert hat.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske mit Flags, die Benachrichtigungsereignisse signalisiert. Die folgenden Flags können vom MAPI-Spooler bei der Eingabe festgelegt werden und müssen bei der Ausgabe unverändert zurückgegeben werden:
    
NOTIFY_ABORT_DEFERRED 
  
> Benachrichtigt den Transportanbieter, dass eine Nachricht, für die er die Verantwortung übernommen hat, zurückgestellt wird. Dieses Flag muss nur von Transportanbietern unterstützt werden, die die Verschiebung unterstützen. Der  _lppvData-Parameter_ zeigt auf den Eintragsbezeichner der abgebrochenen Nachricht. Nachrichten, die der MAPI-Spooler nicht verarbeitet hat, können weiterhin durch Aufrufen der [IMsgStore::AbortSubmit-Methode zurückgestellt](imsgstore-abortsubmit.md) werden. 
    
NOTIFY_BEGIN_INBOUND 
  
> Der MAPI-Spooler kann nun eingehende Nachrichten für diese Transportanbietersitzung akzeptieren. Der MAPI-Spooler ruft regelmäßig die [IXPLogon::P oll-Methode](ixplogon-poll.md) auf, wenn der Transportanbieter das LOGON_SP_POLL-Flag mit dem [IXPProvider::TransportLogon-Aufruf](ixpprovider-transportlogon.md) bei der Anmeldung festgelegt hat. Nachdem das NOTIFY_BEGIN_INBOUND festgelegt wurde, berücksichtigt der MAPI-Spooler das NOTIFY_NEWMAIL-Flag, das im Aufruf der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) übergeben wurde. Die Zeile "Statustabelle" für die Transportanbietersitzung sollte aktualisiert werden, bevor sie durch Aufrufen der [IMAPISupport::ModifyStatusRow-Methode zurückkehrt.](imapisupport-modifystatusrow.md) Die NOTIFY_BEGIN_INBOUND und NOTIFY_END_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Signalisiert dem Transportanbieter, eingehende Nachrichten so schnell wie möglich zu durchrunden. Um diese Benachrichtigung zu erfüllen, sollte der Transportanbieter das STATUS_INBOUND_FLUSH-Flag in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft der Statustabelle so schnell wie möglich mithilfe von **ModifyStatusRow festlegen.** Ein eingehender Messagingzyklus ist abgeschlossen, wenn der Anbieter feststellt, dass er alles heruntergeladen hat, was er kann, oder wenn er einen **TransportNotify-Methodenaufruf** mit dem NOTIFY_END_INBOUND_FLUSH empfangen hat. Bis zum Ende des eingehenden Messagingzyklus sollte der Anbieter die [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) nicht aufrufen oder Zyklen auf andere Weise an das Betriebssystem abliefern, um die Zustellung eingehender Nachrichten zu beschleunigen. Dies ist akzeptabel, da der MAPI-Spooler NOTIFY_BEGIN_INBOUND_FLUSH in der Regel nur als Reaktion auf die Anforderung eines Benutzers über eine Clientanwendung verwendet, um jetzt alle Nachrichten zu senden. Am Ende des eingehenden Leervorgangs sollte der Anbieter **SpoolerNotify** verwenden, um das STATUS_INBOUND_FLUSH in der **PR_STATUS_CODE-Eigenschaft** der Statuszeile zu löschen. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ausgehende Vorgänge können jetzt für diese Transportanbietersitzung auftreten. Wenn nachrichten für diesen Anbieter gesendet werden sollen, folgt ein Aufruf der [IXPLogon::SubmitMessage-Methode.](ixplogon-submitmessage.md) Die Zeile der Statustabelle für diese Sitzung sollte vor der Rückgabe aktualisiert werden. Die NOTIFY_BEGIN_OUTBOUND und NOTIFY_END_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie das NOTIFY_BEGIN_INBOUND_FLUSH, bezieht sich jedoch auf ausgehende Nachrichten. Das entsprechende Statusflag ist STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Der MAPI-Spooler muss die Übertragung der Nachricht abbrechen, für die der  _lppvData-Parameter_ vom **IXPLogon::SubmitMessage-Methodenaufruf** auf den 32-Bit-Wert verweist. Das NOTIFY_CANCEL_MESSAGE kann festgelegt werden, ohne dass der Transportanbieter vom **SubmitMessage-,** **IXPLogon::StartMessage-** oder **IXPLogon::EndMessage-Methodenaufruf** zurückgegeben wurde, der der Nachricht zugeordnet ist. Der Transportanbieter muss so schnell wie möglich vom Einstiegspunkt zurückgeben, der die abgebrochene Nachricht abhanden kommt. Für eine eingehende Nachricht, die derzeit verarbeitet wird, sollte der Transportanbieter die eingehende Nachricht überall speichern, wo sie derzeit gespeichert ist, und sie zum nächsten geeigneten Zeitpunkt erneut zu senden. Die daten des Nachrichtenobjekts, die bereits für die eingehende Nachricht gespeichert sind, werden verworfen. Wenn der Transportanbieter diesen 32-Bit-Wert nicht zur **StartMessage-** oder **SubmitMessage-Zeit** aktualisiert hat, ist der Wert 0 für ausgehende Nachrichten und 1 für eingehende Nachrichten. 
    
NOTIFY_END_INBOUND 
  
> Eingehende Vorgänge müssen für diese Transportanbietersitzung beendet werden. Der MAPI-Spooler verwendet die **Poll-Methode** nicht mehr und ignoriert NOTIFY_NEWMAIL für diese Sitzung. In-Process-Nachrichten sollten abgeschlossen werden. Die Zeile der Statustabelle für die Transportsitzung sollte aktualisiert werden, indem [Sie ModifyStatusRow aufrufen,](imapisupport-modifystatusrow.md) bevor Sie zurückkehren. Die NOTIFY_END_INBOUND und NOTIFY_BEGIN_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Benachrichtigt den Transportanbieter, den eingehenden Leermodus zu verlassen. Der Transportanbieter sollte das Herunterladen nicht beenden, das Herunterladen sollte jedoch im Hintergrund ausgeführt werden. Die Zeile der Statustabelle für die Transportsitzung sollte durch Aufrufen von **ModifyStatusRow** aktualisiert werden, wenn der Transportanbieter diese Benachrichtigung erfüllen kann. 
    
NOTIFY_END_OUTBOUND 
  
> Ausgehende Vorgänge müssen für diese Transportanbietersitzung beendet werden. Der MAPI-Spooler beendet den Aufruf von **SubmitMessage** und ignoriert das **SpoolerNotify-NOTIFY_READYTOSEND** Flag. Wenn derzeit eine ausgehende Nachricht gesendet wird, sollte sie nicht beendet werden. Um die Zustellung einer Nachricht zu beenden, verwenden Sie das NOTIFY_CANCEL_MESSAGE Flag. Die Zeile der Statustabelle für diese Sitzung sollte aktualisiert werden, indem **Sie ModifyStatusRow aufrufen,** bevor Sie zurückkehren. Die NOTIFY_END_INBOUND und NOTIFY_BEGIN_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie NOTIFY_END_INBOUND_FLUSH, bezieht sich jedoch auf ausgehende Nachrichten. Das entsprechende Statusflag ist STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Ein Zeiger auf einen Zeiger auf ereignisspezifische Daten. Weitere Informationen dazu, _was lppvData_ angibt, finden Sie in der Beschreibung für den _lpulFlags-Parameter._ 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::TransportNotify-Methode auf,** um den Transportanbieter über Ereignisse zu signalisieren, für die eine Benachrichtigung angefordert wurde. Diese Ereignisse umfassen eine MAPI-Spooleranforderung zum Abbrechen einer Nachrichtenübertragung, den Anfang oder das Ende eingehender oder ausgehender Transportvorgänge sowie den Anfang oder das Ende eines Vorgangs zum Löschen einer eingehenden oder ausgehenden Nachrichtenwarteschlange. 
  
Wenn der Benutzer versucht, eine Nachricht abgesagt zu haben, die der Transportanbieter zuvor zurückgestellt hat, ruft der MAPI-Spooler **TransportNotify** auf und über NOTIFY_ABORT_DEFERRED- und NOTIFY_CANCEL_MESSAGE-Flags in  _ulFlags_. Wenn sich der MAPI-Spooler abmeldet und weiterhin Nachrichten in der Warteschlange hat, übergibt er nur NOTIFY_ABORT_DEFERRED in _ulFlags,_ wenn er **TransportNotify aufruft.**
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Anbieter muss den Zugriff auf seine Daten bei diesem Aufruf synchronisieren, da der MAPI-Spooler diese Methode aus einem anderen Ausführungsthread oder aus einer Prozedur für ein anderes Fenster aufrufen kann. Dies tritt höchstwahrscheinlich auf, wenn der MAPI-Spooler den Abbruch einer Nachricht signalisiert, die der Transportanbieter gesendet hat.
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

