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
  
Gibt an, dass der MAPI-Spooler eine Nachricht für den zu übermittelnden Transportanbieter hat.
  
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
  
> in Eine Bitmaske von Flags, die die Übermittlung der Nachricht steuert. Das folgende Flag kann festgelegt werden:
    
BEGIN_DEFERRED 
  
> Der MAPI-Spooler Ruft einen Transportanbieter mit einer zuvor verzögerten Meldung auf. Die Eintrags-ID der Nachricht ist identisch mit dem Zeitpunkt, zu dem Sie verzögert wurde. Die Nachricht wurde verzögert, indem die Eintrags-ID mithilfe der [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag zurück an den MAPI-Spooler übergeben wurde. 
    
 _lpMessage_
  
> in Ein Zeiger auf ein Nachrichtenobjekt (das die zu übermittelnde Nachricht darstellt), die über Lese-/Schreibzugriff verfügt, die der Transportanbieter zum zugreifen und Bearbeiten dieser Nachricht verwendet. Dieses Objekt bleibt gültig, bis der Transportanbieter von einem nachfolgenden Aufruf an die [IXPLogon:: EndMessage](ixplogon-endmessage.md) -Methode zurückkehrt. 
    
 _lpulMsgRef_
  
> Out Ein Zeiger auf eine Variable, in der der Transportanbieter den Referenzwert zurückgibt, der dieser Nachricht zugewiesen wurde. Der MAPI-Spooler übergibt diesen Verweiswert in nachfolgenden Aufrufen für diese Nachricht. Der MAPI-Spooler initialisiert den Wert mit 0, bevor er an den Transportanbieter zurückgegeben wird.
    
 _lpulReturnParm_
  
> Out Ein Zeiger auf eine Variable, die dem von **SubmitMessage**zurückgegebenen MAPI_E_WAIT-oder MAPI_E_NETWORK_ERROR-Fehlerwert entspricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
MAPI_E_BUSY 
  
> Der Transportanbieter kann die Nachricht nicht verarbeiten, da Sie einen anderen Vorgang ausführt. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung aufgetreten ist und dass der MAPI-Spooler nicht **EndMessage**aufrufen sollte. Der MAPI-Spooler versucht den **SubmitMessage** -Aufruf später erneut. 
    
MAPI_E_CANCEL 
  
> Obwohl der Transportanbieter angefordert hat, dass der MAPI-Spooler die Nachricht bei einem vorherigen **SpoolerNotify** -Aufruf erneut übermitteln muss, wurden die Bedingungen seither geändert, und die Nachricht sollte nicht erneut gesendet werden. Der MAPI-Spooler wird mit etwas anderem umgehen. 
    
MAPI_E_NETWORK_ERROR 
  
> Ein Netzwerkfehler hat den erfolgreichen Abschluss des Vorgangs verhindert. Der _lpulReturnParm_ -Parameter sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen, bevor die Nachricht vom MAPI-Spooler erneut übermittelt wird. 
    
MAPI_E_NOT_ME 
  
> Der Transportanbieter kann diese Nachricht nicht verarbeiten. Der MAPI-Spooler sollte versuchen, einen anderen Transportanbieter für diesen zu finden. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung aufgetreten ist und dass der MAPI-Spooler nicht **EndMessage**aufrufen sollte.
    
MAPI_E_WAIT 
  
> Ein vorübergehendes Problem verhindert, dass der Transportanbieter die Nachricht verarbeitet. Der _lpulReturnParm_ -Parameter sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen, bevor die Nachricht vom MAPI-Spooler erneut übermittelt wird. 
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPLogon:: SubmitMessage** -Methode auf, wenn eine Nachricht für den zu übermittelnden Transportanbieter vorliegt. Die Nachricht wird mithilfe des _lpMessage_ -Parameters an den Transportanbieter übergeben. 
  
Wenn der Anbieter bereit ist, die Nachricht zu akzeptieren, sollte Sie einen Verweiswert zurückgeben, indem Sie den _lpulMsgRef_ -Parameter verwenden, das übergebene Objekt verarbeiten und den entsprechenden Wert (normalerweise S_OK) zurückgeben. Wenn der Anbieter nicht bereit ist, die Übertragung zu verarbeiten, sollte er einen Fehlerwert und optional einen weiteren MAPI-Rückgabewert in _lpulReturnParm_ zurückgeben, um anzugeben, wie lange der MAPI-Spooler warten soll, bevor die Nachricht erneut übermittelt wird. 
  
Die Implementierung dieser Methode durch einen Transportanbieter kann folgende Aktionen ausführen:
  
- Setzen Sie die Nachricht in eine interne Warteschlange, um auf die Übertragung zu warten, möglicherweise die Nachricht in den lokalen Speicher zu kopieren und zurückzugeben.
    
- Versuchen Sie, die tatsächliche Übertragung und Rückgabe zu erreichen, wenn die Übertragung erfolgreich oder erfolglos abgeschlossen wurde.
    
- Bestimmen Sie, ob die Nachricht nach dem Überprüfen der betreffenden Ressource gesendet werden soll. In diesem Fall kann der Anbieter, wenn die Ressource frei ist, die Ressource sperren, die Nachricht vorbereiten und übermitteln. Wenn die Ressource ausgelastet ist, kann der Anbieter die Nachricht vorbereiten und das Senden zu einem späteren Zeitpunkt aufschieben.
    
Die bevorzugte Technik für die Nachrichtenübermittlung hängt vom Transportanbieter und der erwarteten Anzahl von Prozessen ab, die für Systemressourcen konkurrieren. 
  
Während eines **SubmitMessage** -Aufrufs steuert der Transportanbieter die Übermittlung von Nachrichtendaten aus dem Nachrichtenobjekt. Der Transportanbieter sollte der Nachricht jedoch einen Verweiswert zuweisen, dem Sie vor dem Übertragen von Daten einen Zeiger in _lpulMsgRef_zurückgibt. Dies ist der Fall, da der MAPI-Spooler zu einem beliebigen Zeitpunkt während des Vorgangs die [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode aufrufen kann, wobei das NOTIFY_CANCEL_MESSAGE-Flag festgelegt ist, um den Anbieter zu signalisieren, dass alle geöffneten Objekte freigegeben und die Nachrichtenübertragung beendet werden soll. 
  
Der Transportanbieter sollte keine nicht übertragbaren Eigenschaften der Nachricht senden. Wenn Sie eine solche Eigenschaft findet, sollte Sie fortfahren, um die Next-Eigenschaft zu verarbeiten. Der Anbieter sollte sich bemühen, keine MAPI_P1-Empfängerinformationen als Teil des übertragenen Nachrichteninhalts anzuzeigen. der Anbieter sollte diese Empfängerinformationen nur zu Adressierungs Zwecken verwenden. MAPI_P1-Empfänger sind intern generierte Empfänger, die zum erneuten Senden von Nachrichten verwendet werden. Sie sollten nicht übertragen werden. Verwenden Sie stattdessen die anderen Empfänger für die Übertragung von Empfängerinformationen. Der Zweck dieser Anordnung besteht darin, es den erneuten Empfängern zu gestatten, genau dieselbe Empfängertabelle wie die ursprünglichen Empfänger anzuzeigen.
  
Während eines **SubmitMessage** -Aufrufs verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und verarbeitet Anlagen. Diese Verarbeitung kann sehr viel Zeit in Anspruch nehmen. Transport Anbieter können die [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) -Methode für den MAPI-Spooler während dieser Verarbeitung häufig aufrufen, um die CPU-Zeit für andere Systemaufgaben zu veröffentlichen. 
  
Alle Nachrichtenempfänger sind in der Empfängertabelle der Nachricht sichtbar, die der MAPI-Spooler ursprünglich übergeben hat. Der Transportanbieter sollte nur die Empfänger verarbeiten, die er verarbeiten kann – basierend auf der Eintrags-ID, dem Adresstyp oder beiden – und die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft nicht bereits auf true festgelegt haben. Wenn **PR_RESPONSIBILITY** bereits auf true festgelegt ist, hat ein anderer Transportanbieter diesen Empfänger behandelt. Wenn der Anbieter eine ausreichende Verarbeitung eines Empfängers abgeschlossen hat, um zu bestimmen, ob er Nachrichten für diesen Empfänger verarbeiten kann, sollte er die **PR_RESPONSIBILITY** -Eigenschaft des Empfängers in der übergebenen Nachricht auf true festlegen. In der Regel trifft der Anbieter diese Bestimmung nach Abschluss der Nachrichtenübermittlung. 
  
In der Regel wird der Transportanbieter nicht von einem **SubmitMessage** -Aufruf zurückgegeben, bis die Übermittlung der Nachrichtendaten abgeschlossen ist. Wenn kein Fehler zurückgegeben wird, ist der nächste Aufruf des MAPI-Spoolers an den Anbieter ein Aufruf der [IXPLogon:: EndMessage](ixplogon-endmessage.md) -Methode. 
  
Wenn **SubmitMessage** einen Fehler zurückgibt, gibt der MAPI-Spooler die Nachricht in Process frei, ohne Änderungen zu speichern. Wenn der Transportanbieter das Speichern von Nachrichtenänderungen erfordert, muss er die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht aufrufen, bevor Sie zurückgegeben wird. 
  
Bei Fehlern, die aufgrund von Transportproblemen auftreten, behält die MAPI-Warteschlange die Nachricht bei, verzögert jedoch die erneute Übermittlung der Nachricht an den Transportanbieter basierend auf dem in _lpulReturnParm_zurückgegebenen Wert. Der Transportanbieter muss diesen Wert angeben, wenn der Rückgabewert von **SUBMITMESSAGE** MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR ist. Wenn eine schwere Fehlerbedingung auftritt, muss der Transportanbieter die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_CRITICAL_ERROR-Flag aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

