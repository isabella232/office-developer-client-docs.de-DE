---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7a53fb7f07be66c1d55f1adabc24511c9d50bb84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592200"
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
  
> [in, out] Eine Bitmaske mit Flags, die Benachrichtigungsereignisse signalisiert. Die folgenden Flags können vom MAPI-Spooler für die Eingabe festgelegt werden und müssen bei der Ausgabe unverändert zurückgegeben werden:
    
NOTIFY_ABORT_DEFERRED 
  
> Benachrichtigt den Transportanbieter, dass eine Nachricht, für die er die Verantwortung akzeptiert hat, zurückgestellt wird. Nur Transportanbieter, die Verzögerung unterstützen, müssen dieses Flag unterstützen. Der  _lppvData-Parameter_ verweist auf den Eintragsbezeichner der abgebrochenen Nachricht. Nachrichten, die der MAPI-Spooler nicht verarbeitet hat, können durch Aufrufen der [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) zurückgestellt werden. 
    
NOTIFY_BEGIN_INBOUND 
  
> Der MAPI-Spooler kann nun eingehende Nachrichten für diese Transportanbietersitzung akzeptieren. Der MAPI-Spooler ruft regelmäßig die [IXPLogon::P oll-Methode](ixplogon-poll.md) auf, wenn der Transportanbieter das LOGON_SP_POLL Flag mit dem [IXPProvider::TransportLogon-Aufruf](ixpprovider-transportlogon.md) bei der Anmeldung festgelegt hat. Sobald das NOTIFY_BEGIN_INBOUND Flag festgelegt ist, berücksichtigt der MAPI-Spooler das NOTIFY_NEWMAIL Flag, das im Aufruf der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) übergeben wurde. Die Zeile der Statustabelle für die Transportanbietersitzung sollte vor der Rückgabe durch Aufrufen der [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aktualisiert werden. Die Flags NOTIFY_BEGIN_INBOUND und NOTIFY_END_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Signalisiert dem Transportanbieter, eingehende Nachrichten so schnell wie möglich zu durchlaufen. Um dieser Benachrichtigung zu entsprechen, sollte der Transportanbieter das flag STATUS_INBOUND_FLUSH in der **Eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) seiner Statustabellenzeile so schnell wie möglich mithilfe von **ModifyStatusRow** festlegen. Ein eingehender Nachrichtenzyklus ist abgeschlossen, wenn der Anbieter feststellt, dass er alles heruntergeladen hat, was er kann, oder wenn er einen **TransportNotify-Methodenaufruf** mit festgelegter NOTIFY_END_INBOUND_FLUSH-Flag erhalten hat. Bis zum Ende des eingehenden Nachrichtenzyklus sollte der Anbieter die [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) nicht aufrufen oder auf andere Weise Zyklen an das Betriebssystem übertragen, um die Zustellung eingehender Nachrichten zu beschleunigen. Dies ist akzeptabel, da der MAPI-Spooler in der Regel NOTIFY_BEGIN_INBOUND_FLUSH nur als Reaktion auf die Anforderung eines Benutzers über eine Clientanwendung verwendet, um jetzt alle Nachrichten zu übermitteln. Am Ende des Vorgangs für die eingehende Leerung sollte der Anbieter **SpoolerNotify** verwenden, um das STATUS_INBOUND_FLUSH Flag in der **PR_STATUS_CODE** Eigenschaft der Statuszeile zu löschen. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ausgehende Vorgänge können jetzt für diese Transportanbietersitzung auftreten. Wenn für diesen Anbieter Nachrichten gesendet werden sollen, folgt ein Aufruf der [IXPLogon::SubmitMessage-Methode.](ixplogon-submitmessage.md) Die Zeile der Statustabelle für diese Sitzung sollte vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_BEGIN_OUTBOUND und NOTIFY_END_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie das NOTIFY_BEGIN_INBOUND_FLUSH Flag, bezieht sich jedoch auf ausgehende Nachrichten. Das entsprechende Status-Flag ist STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Der MAPI-Spooler muss die Übertragung der Nachricht abbrechen, für die der  _lppvData-Parameter_ auf den 32-Bit-Wert aus dem Aufruf der **IXPLogon::SubmitMessage-Methode** zeigt. Das NOTIFY_CANCEL_MESSAGE Kennzeichen kann festgelegt werden, ohne dass der Transportanbieter vom **SubmitMessage-,** **IXPLogon::StartMessage-** oder **IXPLogon::EndMessage-Methodenaufruf** zurückgegeben wurde, der der Nachricht zugeordnet ist. Der Transportanbieter muss so schnell wie möglich vom Einstiegspunkt, der die abgebrochene Nachricht verarbeitet, zurückkehren. Bei einer eingehenden Nachricht, die derzeit verarbeitet wird, sollte der Transportanbieter die eingehende Nachricht überall dort speichern, wo sie gerade gespeichert ist, und sie zum nächsten geeigneten Zeitpunkt erneut übermitteln. Die bereits für die eingehende Nachricht gespeicherten Nachrichtenobjektdaten werden verworfen. Wenn der Transportanbieter diesen 32-Bit-Wert zur **StartMessage-** oder **SubmitMessage-Zeit** nicht aktualisiert hat, ist der Wert 0 für ausgehende Nachrichten und 1 für eingehende Nachrichten. 
    
NOTIFY_END_INBOUND 
  
> Eingehende Vorgänge müssen für diese Transportanbietersitzung eingestellt werden. Der MAPI-Spooler verwendet nicht mehr die **Poll-Methode** und ignoriert NOTIFY_NEWMAIL für diese Sitzung. In-Process-Nachrichten sollten abgeschlossen werden. Die Statustabellenzeile für die Transportsitzung sollte durch Aufrufen von [ModifyStatusRow](imapisupport-modifystatusrow.md) vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Benachrichtigt den Transportanbieter, dass der eingehende Leermodus beendet wird. Der Transportanbieter sollte den Download nicht beenden, aber das Herunterladen sollte im Hintergrund erfolgen. Die Statustabellenzeile für die Transportsitzung sollte durch Aufrufen von **ModifyStatusRow** aktualisiert werden, wenn der Transportanbieter diese Benachrichtigung erfüllen kann. 
    
NOTIFY_END_OUTBOUND 
  
> Ausgehende Vorgänge müssen für diese Transportanbietersitzung eingestellt werden. Der MAPI-Spooler ruft **submitMessage** nicht mehr auf und ignoriert das **Flag "SpoolerNotify"** NOTIFY_READYTOSEND. Wenn derzeit eine ausgehende Nachricht gesendet wird, sollte sie nicht beendet werden. Um die Zustellung einer Nachricht zu beenden, verwenden Sie das NOTIFY_CANCEL_MESSAGE Flag. Die Zeile der Statustabelle für diese Sitzung sollte durch Aufrufen von **ModifyStatusRow** vor der Rückgabe aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie NOTIFY_END_INBOUND_FLUSH, bezieht sich jedoch auf ausgehende Nachrichten. Das entsprechende Status-Flag ist STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Ein Zeiger auf einen Zeiger auf ereignisspezifische Daten. Weitere Informationen dazu, was _lppvData_ angibt, finden Sie in der Beschreibung des _lpulFlags-Parameters._ 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::TransportNotify-Methode** auf, um dem Transportanbieter zu Ereignissen zu signalisieren, für die eine Benachrichtigung angefordert wurde. Diese Ereignisse umfassen eine MAPI-Spooleranforderung zum Abbrechen einer Nachrichtenübertragung, den Anfang oder das Ende von eingehenden oder ausgehenden Transportvorgängen und den Anfang oder das Ende eines Vorgangs zum Löschen einer eingehenden oder ausgehenden Nachrichtenwarteschlange. 
  
Wenn der Benutzer versucht, eine Nachricht abzubrechen, die der Transportanbieter zuvor zurückgestellt hat, ruft der MAPI-Spooler **TransportNotify** auf und übergibt die Flags NOTIFY_ABORT_DEFERRED und NOTIFY_CANCEL_MESSAGE in  _ulFlags_. Wenn sich der MAPI-Spooler abmeldet und weiterhin Nachrichten in der Warteschlange enthält, übergibt er beim Aufrufen von **TransportNotify** nur NOTIFY_ABORT_DEFERRED in _ulFlags._
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Anbieter muss den Zugriff auf seine Daten bei diesem Aufruf synchronisieren, da der MAPI-Spooler diese Methode von einem anderen Ausführungsthread oder von einer Prozedur für ein anderes Fenster aufrufen kann. Dies tritt höchstwahrscheinlich auf, wenn der MAPI-Spooler den Abbruch einer Nachricht signalisiert, die vom Transportanbieter gesendet wurde.
  
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

