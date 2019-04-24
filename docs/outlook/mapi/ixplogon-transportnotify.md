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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351562"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Signalisiert das Eintreffen eines Ereignisses, über das der Transportanbieter eine Benachrichtigung angefordert hat.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in, out] Eine Bitmaske von Flags, die Benachrichtigungsereignisse signalisiert. Die folgenden Flags können vom MAPI-Spooler bei der Eingabe festgelegt werden und müssen bei der Ausgabe unverändert zurückgegeben werden:
    
NOTIFY_ABORT_DEFERRED 
  
> Benachrichtigt den Transportanbieter, dass eine Nachricht, für die die Verantwortung übernommen wurde, verzögert wird. Nur Transportanbieter, die eine Verschiebung unterstützen, müssen dieses Flag unterstützen. Der _lppvData_ -Parameter verweist auf die Eintrags-ID der abgebrochenen Nachricht. Nachrichten, die der MAPI-Spooler nicht verarbeitet hat, können weiterhin durch Aufrufen der [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) -Methode verzögert werden. 
    
NOTIFY_BEGIN_INBOUND 
  
> Der MAPI-Spooler kann jetzt eingehende Nachrichten für diese Transportanbieter Sitzung akzeptieren. Der MAPI-Spooler ruft regelmäßig die [IXPLogon::P oll](ixplogon-poll.md) -Methode auf, wenn der Transportanbieter das LOGON_SP_POLL-Flag mit dem [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Aufruf bei der Anmeldung festgelegt hat. Nachdem das NOTIFY_BEGIN_INBOUND-Flag festgelegt wurde, ehrt der MAPI-Spooler das NOTIFY_NEWMAIL-Flag, das beim Aufruf der [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode übergeben wird. Die Statustabellen Zeile für die Transportanbieter Sitzung sollte vor dem zurückgeben durch Aufrufen der [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aktualisiert werden. Die Flags NOTIFY_BEGIN_INBOUND und NOTIFY_END_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Signalisiert, dass der Transportanbieter eingehende Nachrichten so schnell wie möglich durchlaufen soll. Zur Einhaltung dieser Benachrichtigung muss der Transportanbieter das STATUS_INBOUND_FLUSH-Flag in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft der Status Tabellenzeile so schnell wie möglich festlegen, indem Sie **ModifyStatusRow**verwenden. Ein eingehender Messaging Zyklus ist abgeschlossen, wenn der Anbieter feststellt, dass er alle möglicherweise heruntergeladen hat, oder wenn er einen **TransportNotify** -Methodenaufruf mit dem NOTIFY_END_INBOUND_FLUSH-Kennzeichen Satz erhalten hat. Bis zum Ende des eingehenden Messaging Zyklus sollte der Anbieter die [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) -Methode nicht aufrufen oder anderweitig Zyklen an das Betriebssystem abgeben, um die Übermittlung eingehender Nachrichten zu beschleunigen. Dies ist akzeptabel, da der MAPI-Spooler in der Regel NOTIFY_BEGIN_INBOUND_FLUSH nur als Reaktion auf die Anforderung eines Benutzers über eine Clientanwendung verwendet, um alle Nachrichten jetzt zuzustellen. Am Ende des eingehenden Flush-Vorgangs sollte der Anbieter **SpoolerNotify** verwenden, um das STATUS_INBOUND_FLUSH-Flag in der **PR_STATUS_CODE** -Eigenschaft seiner Status Zeile zu löschen. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Ausgehende Vorgänge können nun für diese Transportanbieter Sitzung ausgeführt werden. Wenn für diesen Anbieter Nachrichten gesendet werden, folgt ein Aufruf der [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode. Die Statustabellen Zeile für diese Sitzung sollte vor dem zurückgeben aktualisiert werden. Die Flags NOTIFY_BEGIN_OUTBOUND und NOTIFY_END_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie das NOTIFY_BEGIN_INBOUND_FLUSH-Flag, verweist jedoch auf ausgehende Nachrichten. Das entsprechende Statuskennzeichen ist STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Der MAPI-Spooler muss die Übertragung der Nachricht abbrechen, für die der _lppvData_ -Parameter auf den 32-Bit-Wert vom **IXPLogon:: SubmitMessage** -Methodenaufruf zeigt. Das NOTIFY_CANCEL_MESSAGE-Flag kann festgelegt werden, ohne dass der Transportanbieter vom **SubmitMessage**, **IXPLogon:: StartMessage**oder **IXPLogon:: EndMessage** -Methodenaufruf zurückgegeben wird, der der Nachricht zugeordnet ist. Der Transportanbieter muss so schnell wie möglich vom Einstiegspunkt zurückkehren, der die abgebrochene Nachricht verarbeitet. Für eine eingehende Nachricht, die derzeit verarbeitet wird, sollte der Transportanbieter die eingehenden Nachrichten speichern, wo Sie derzeit gespeichert ist, und Sie zum nächsten bequemen Zeitpunkt erneut bereitstellen. Die Daten des Nachrichtenobjekts, die bereits für die eingehende Nachricht gespeichert wurden, werden verworfen. Wenn der Transportanbieter diesen 32-Bit-Wert nicht zur **StartMessage** -oder **SubmitMessage** -Zeit aktualisiert hat, ist der Wert 0 für ausgehende Nachrichten und 1 für eingehende Nachrichten. 
    
NOTIFY_END_INBOUND 
  
> Eingehende Vorgänge müssen für diese Transportanbieter Sitzung beendet werden. Der MAPI-Spooler beendet die Verwendung der **Poll** -Methode und ignoriert NOTIFY_NEWMAIL für diese Sitzung. In-Process-Nachrichten sollten abgeschlossen sein. Die Statustabellen Zeile für die Transportsitzung sollte durch Aufrufen von [ModifyStatusRow](imapisupport-modifystatusrow.md) vor dem zurückgeben aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_INBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Benachrichtigt den Transportanbieter, dass er den eingehenden Flush-Modus ausgibt. Der Transportanbieter sollte den Download nicht beenden, das herunterladen sollte jedoch im Hintergrund erfolgen. Die Statustabellen Zeile für die Transportsitzung sollte durch Aufrufen von **ModifyStatusRow** aktualisiert werden, wenn der Transportanbieter diese Benachrichtigung einhalten kann. 
    
NOTIFY_END_OUTBOUND 
  
> Ausgehende Vorgänge müssen für diese Transportanbieter Sitzung beendet werden. Der MAPI-Spooler beendet den Aufruf von **SubmitMessage** und ignoriert das **SpoolerNotify** -NOTIFY_READYTOSEND-Flag. Wenn eine ausgehende Nachricht derzeit gesendet wird, sollte Sie nicht beendet werden; um die Übermittlung einer Nachricht zu beenden, verwenden Sie das NOTIFY_CANCEL_MESSAGE-Flag. Die Statustabellen Zeile für diese Sitzung sollte durch Aufrufen von **ModifyStatusRow** vor dem zurückgeben aktualisiert werden. Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_OUTBOUND schließen sich gegenseitig aus. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Funktioniert ähnlich wie NOTIFY_END_INBOUND_FLUSH, bezieht sich jedoch auf ausgehende Nachrichten. Das entsprechende Statuskennzeichen ist STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> Out Ein Zeiger auf einen Zeiger auf ereignisspezifische Daten. Weitere Informationen dazu, was von _lppvData_ angegeben wird, finden Sie in der Beschreibung des Parameters _lpulFlags_ . 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPLogon:: TransportNotify** -Methode auf, um den Transportanbieter über Ereignisse zu signalisieren, für die eine Benachrichtigung angefordert wurde. Diese Ereignisse enthalten eine MAPI-Spooler-Anforderung zum Abbrechen einer Nachrichtenübertragung, den Anfang oder das Ende des eingehenden oder ausgehenden Transports und den Anfang oder das Ende eines Vorgangs, um eine eingehende oder ausgehende Nachrichtenwarteschlange zu löschen. 
  
Wenn der Benutzer versucht, eine Nachricht abzubrechen, die der Transportanbieter zuvor zurückgestellt hat, ruft der MAPI-Spooler **TransportNotify**auf und übergibt sowohl die NOTIFY_ABORT_DEFERRED-als auch die NOTIFY_CANCEL_MESSAGE-Flags in _ulFlags_. Wenn sich der MAPI-Spooler abmeldet und weiterhin Nachrichten in der Warteschlange aufweist, übergibt er nur NOTIFY_ABORT_DEFERRED in _ulFlags_ , wenn er **TransportNotify**aufruft.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Anbieter muss den Zugriff auf seine Daten für diesen Aufruf synchronisieren, da der MAPI-Spooler diese Methode von einem anderen Ausführungsthread oder von einer Prozedur für ein anderes Fenster aus aufrufen kann. Dies wird wahrscheinlich auftreten, wenn der MAPI-Spooler den Abbruch einer Nachricht signalisiert, die der Transportanbieter mit dem Senden begonnen hat.
  
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

