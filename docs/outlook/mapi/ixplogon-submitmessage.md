---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423321"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass der MAPI-Spooler über eine Nachricht verfügt, die der Transportanbieter zu liefern hat.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachricht übermittelt wird. Das folgende Flag kann festgelegt werden:
    
BEGIN_DEFERRED 
  
> Der MAPI-Spooler ruft einen Transportanbieter mit einer Nachricht auf, die zuvor verzögert wurde. Der Eintragsbezeichner der Nachricht ist identisch mit dem, als sie zurückgestellt wurde. Die Nachricht wurde zurückgestellt, indem der Eintragsbezeichner mithilfe der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem NOTIFY_SENTDEFERRED übergeben wurde. 
    
 _lpMessage_
  
> [in] Ein Zeiger auf ein Nachrichtenobjekt (das die zu liefernde Nachricht darstellt), das über Lese-/Schreibberechtigungen verfügt, die der Transportanbieter verwendet, um auf diese Nachricht zu zugreifen und diese zu bearbeiten. Dieses Objekt bleibt gültig, bis der Transportanbieter von einem nachfolgenden Aufruf der [IXPLogon::EndMessage-Methode zurückkehrt.](ixplogon-endmessage.md) 
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf eine Variable, in der der Transportanbieter den Dieser Nachricht zugewiesenen Referenzwert zurückgibt. Der MAPI-Spooler übergibt diesen Referenzwert in nachfolgenden Aufrufen für diese Nachricht. Der MAPI-Spooler initialisiert den Wert auf 0, bevor er an den Transportanbieter zurückvermittelt wird.
    
 _lpulReturnParm_
  
> [out] Ein Zeiger auf eine Variable, die dem MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR von **SubmitMessage** zurückgegebenen Fehlerwert entspricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Der Transportanbieter kann die Nachricht nicht verarbeiten, da er einen anderen Vorgang ausführen kann. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung erfolgt ist und der MAPI-Spooler **nicht EndMessage aufrufen sollte.** Der MAPI-Spooler versucht den **SubmitMessage-Aufruf** später erneut. 
    
MAPI_E_CANCEL 
  
> Obwohl der Transportanbieter angefordert hat, dass der MAPI-Spooler die Nachricht bei einem vorherigen **SpoolerNotify-Aufruf** erneut übermittelt, haben sich die Bedingungen seitdem geändert, und die Nachricht sollte nicht erneut gesendet werden. Der MAPI-Spooler wird dann etwas anderes verarbeiten. 
    
MAPI_E_NETWORK_ERROR 
  
> Ein Netzwerkfehler verhinderte den erfolgreichen Abschluss des Vorgangs. Der  _lpulReturnParm-Parameter_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen, bevor der MAPI-Spooler die Nachricht erneut übermittelt. 
    
MAPI_E_NOT_ME 
  
> Der Transportanbieter kann diese Nachricht nicht verarbeiten. Der MAPI-Spooler sollte versuchen, einen anderen Transportanbieter dafür zu finden. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung erfolgt ist und der MAPI-Spooler **nicht EndMessage aufrufen sollte.**
    
MAPI_E_WAIT 
  
> Ein temporäres Problem verhindert, dass der Transportanbieter die Nachricht behandeln kann. Der  _lpulReturnParm-Parameter_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen, bevor der MAPI-Spooler die Nachricht erneut übermittelt. 
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::SubmitMessage-Methode** auf, wenn eine Nachricht für den Transportanbieter zu übermitteln ist. Die Nachricht wird mithilfe des  _lpMessage-Parameters_ an den Transportanbieter übergeben. 
  
Wenn der Anbieter bereit ist, die Nachricht zu akzeptieren, sollte er einen Verweiswert mithilfe des  _lpulMsgRef-Parameters_ zurückgeben, das übergebene Objekt verarbeiten und den entsprechenden Wert zurückgeben (in der Regel S_OK). Wenn der Anbieter nicht bereit ist, die Übertragung zu verarbeiten, sollte er einen Fehlerwert und optional einen weiteren MAPI-Rückgabewert in  _lpulReturnParm_ zurückgeben, um anzugeben, wie lange der MAPI-Spooler warten soll, bevor die Nachricht erneut übermittelt wird. 
  
Die Implementierung dieser Methode kann von einem Transportanbieter wie folgt umgesetzt werden:
  
- Legen Sie die Nachricht in eine interne Warteschlange, um auf die Übertragung zu warten, möglicherweise kopieren Sie die Nachricht in den lokalen Speicher, und kehren Sie zurück.
    
- Versuchen Sie, die tatsächliche Übertragung durchzuführen und zurückzukehren, wenn die Übertragung erfolgreich oder erfolglos abgeschlossen ist.
    
- Bestimmen Sie, ob die Nachricht gesendet werden soll, nachdem Sie die ressource überprüft haben. In diesem Fall kann der Anbieter die Ressource sperren, die Nachricht vorbereiten und übermitteln, wenn die Ressource kostenlos ist. Wenn die Ressource ausgelastet ist, kann der Anbieter die Nachricht vorbereiten und das Senden an einen späteren Zeitpunkt zurückfahren.
    
Die bevorzugte Technik für die Nachrichtenübermittlung hängt vom Transportanbieter und der erwarteten Anzahl von Prozessen ab, die um Systemressourcen konkurrieren. 
  
Während eines **SubmitMessage-Aufrufs** steuert der Transportanbieter die Übertragung von Nachrichtendaten aus dem Message-Objekt. Der Transportanbieter sollte der Nachricht jedoch einen Verweiswert zuweisen, zu dem er einen Zeiger in  _lpulMsgRef_ zurückgibt, bevor Daten übertragen werden. Dies ist der Fall, da der MAPI-Spooler jederzeit die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) aufrufen kann, deren NOTIFY_CANCEL_MESSAGE-Flag festgelegt ist, um dem Anbieter zu signalisieren, dass alle geöffneten Objekte freigegeben und die Nachrichtenübertragung beendet werden soll. 
  
Der Transportanbieter sollte keine nichttransmittablen Eigenschaften der Nachricht senden. Wenn eine solche Eigenschaft gefunden wird, sollte sie die nächste Eigenschaft verarbeiten. Der Anbieter sollte alles tun, um keine MAPI_P1 als Teil des übermittelten Nachrichteninhalts anzuzeigen. Der Anbieter sollte diese Empfängerinformationen nur zu Adressierungszwecken verwenden. MAPI_P1 empfänger sind intern generierte Empfänger, die zum erneuten Senden von Nachrichten verwendet werden. sie sollten nicht übertragen werden. Verwenden Sie stattdessen die anderen Empfänger zum Übermitteln von Empfängerinformationen. Zweck dieser Vereinbarung ist es, erneut gesendeten Empfängern zu ermöglichen, genau dieselbe Empfängertabelle wie die ursprünglichen Empfänger zu sehen.
  
Während eines **SubmitMessage-Aufrufs** verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und verarbeitet anlagen. Diese Verarbeitung kann sehr lange dauern. Transportanbieter können die [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) für den MAPI-Spooler während dieser Verarbeitung häufig aufrufen, um die CPU-Zeit für andere Systemaufgaben frei zu geben. 
  
Alle Nachrichtenempfänger sind in der Empfängertabelle der Nachricht sichtbar, die der MAPI-Spooler ursprünglich übergeben hat. Der Transportanbieter sollte nur die Empfänger verarbeiten, die er verarbeiten kann – basierend auf der Eintrags-ID, dem Adresstyp oder beiden – und die ihre **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft noch nicht auf TRUE festgelegt haben. Wenn **PR_RESPONSIBILITY** bereits auf TRUE festgelegt ist, hat ein anderer Transportanbieter den Empfänger verarbeitet. Wenn der Anbieter eine ausreichende Verarbeitung eines Empfängers abgeschlossen hat, um festzustellen, ob er Nachrichten für diesen Empfänger verarbeiten kann, sollte die **PR_RESPONSIBILITY-Eigenschaft** dieses Empfängers in der übergebenen Nachricht auf TRUE festgelegt werden. In der Regel nimmt der Anbieter diese Bestimmung vor, nachdem die Nachrichtenzustellung abgeschlossen ist. 
  
In der Regel gibt der Transportanbieter erst von einem **SubmitMessage-Anruf** zurück, wenn er die Übertragung von Nachrichtendaten abgeschlossen hat. Wenn kein Fehler zurückgegeben wird, ist der nächste Aufruf vom MAPI-Spooler an den Anbieter ein Aufruf der [IXPLogon::EndMessage-Methode.](ixplogon-endmessage.md) 
  
Wenn **SubmitMessage** einen Fehler zurückgibt, gibt der MAPI-Spooler die Nachricht während des Vorgangs frei, ohne Änderungen zu speichern. Wenn für den Transportanbieter Nachrichtenänderungen gespeichert werden müssen, muss er die [IMAPIProp::SaveChanges-Methode für](imapiprop-savechanges.md) die Nachricht aufrufen, bevor er zurückkehrt. 
  
Bei Fehlern, die aufgrund von Transportproblemen auftreten, behält der MAPI-Spooler die Nachricht bei, verzögert jedoch das erneute Senden der Nachricht an den Transportanbieter basierend auf dem in  _lpulReturnParm_ zurückgegebenen Wert. Der Transportanbieter muss den Wert ausfüllen, wenn der Rückgabewert von **SubmitMessage** MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR. Wenn ein schwerwiegender Fehler auftritt, muss der Transportanbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem NOTIFY_CRITICAL_ERROR aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

