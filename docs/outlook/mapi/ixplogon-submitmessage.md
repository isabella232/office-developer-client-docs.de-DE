---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d7a58e0aea54c40f44609dcf51e968762f04edf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571549"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass der MAPI-Spooler über eine Nachricht verfügt, die der Transportanbieter übermitteln soll.
  
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachricht gesendet wird. Das folgende Kennzeichen kann festgelegt werden:
    
BEGIN_DEFERRED 
  
> Der MAPI-Spooler ruft einen Transportanbieter mit einer Nachricht auf, die zuvor zurückgestellt wurde. Der Eintragsbezeichner der Nachricht ist identisch mit dem Zeitpunkt, zu dem sie zurückgestellt wurde. Die Nachricht wurde zurückgestellt, indem der Eintragsbezeichner mithilfe der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem flag NOTIFY_SENTDEFERRED an den MAPI-Spooler übergeben wurde. 
    
 _lpMessage_
  
> [in] Ein Zeiger auf ein Nachrichtenobjekt (das die zuzustellende Nachricht darstellt), das über Lese-/Schreibberechtigungen verfügt, die der Transportanbieter verwendet, um auf diese Nachricht zuzugreifen und sie zu bearbeiten. Dieses Objekt bleibt gültig, bis der Transportanbieter von einem nachfolgenden Aufruf der [IXPLogon::EndMessage-Methode](ixplogon-endmessage.md) zurückgegeben wurde. 
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf eine Variable, in der der Transportanbieter den dieser Nachricht zugewiesenen Referenzwert zurückgibt. Der MAPI-Spooler übergibt diesen Referenzwert in nachfolgenden Aufrufen dieser Nachricht. Der MAPI-Spooler initialisiert den Wert auf 0, bevor er an den Transportanbieter zurückgegeben wird.
    
 _lpulReturnParm_
  
> [out] Ein Zeiger auf eine Variable, die dem von **SubmitMessage** zurückgegebenen MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR Fehlerwert entspricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Der Transportanbieter kann die Nachricht nicht verarbeiten, da sie einen anderen Vorgang ausführt. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung stattgefunden hat und dass der MAPI-Spooler **EndMessage** nicht aufrufen sollte. Der MAPI-Spooler versucht den **SubmitMessage-Aufruf** später erneut. 
    
MAPI_E_CANCEL 
  
> Obwohl der Transportanbieter angefordert hat, dass der MAPI-Spooler die Nachricht bei einem vorherigen **SpoolerNotify-Aufruf** erneut sendet, haben sich die Bedingungen geändert, und die Nachricht sollte nicht erneut übermittelt werden. Der MAPI-Spooler geht weiter, um etwas anderes zu verarbeiten. 
    
MAPI_E_NETWORK_ERROR 
  
> Ein Netzwerkfehler hat den erfolgreichen Abschluss des Vorgangs verhindert. Der  _Parameter lpulReturnParm_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstrichen sind, bevor der MAPI-Spooler die Nachricht erneut sendet. 
    
MAPI_E_NOT_ME 
  
> Der Transportanbieter kann diese Nachricht nicht verarbeiten. Der MAPI-Spooler sollte versuchen, einen anderen Transportanbieter dafür zu finden. Ein Anbieter sollte diesen Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung stattgefunden hat und dass der MAPI-Spooler **EndMessage** nicht aufrufen sollte.
    
MAPI_E_WAIT 
  
> Ein temporäres Problem verhindert, dass der Transportanbieter die Nachricht verarbeitet. Der  _Parameter lpulReturnParm_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstrichen sind, bevor der MAPI-Spooler die Nachricht erneut sendet. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::SubmitMessage-Methode auf,** wenn der Transportanbieter eine Nachricht zu übermitteln hat. Die Nachricht wird mithilfe des  _lpMessage-Parameters_ an den Transportanbieter übergeben. 
  
Wenn der Anbieter bereit ist, die Nachricht zu akzeptieren, sollte er mithilfe des  _lpulMsgRef-Parameters_ einen Verweiswert zurückgeben, das übergebene Objekt verarbeiten und den entsprechenden Wert zurückgeben (in der Regel S_OK). Wenn der Anbieter nicht bereit ist, die Übertragung zu verarbeiten, sollte er einen Fehlerwert und optional einen anderen MAPI-Rückgabewert in  _lpulReturnParm_ zurückgeben, um anzugeben, wie lange der MAPI-Spooler warten soll, bevor die Nachricht erneut übermittelt wird. 
  
Die Implementierung dieser Methode durch einen Transportanbieter kann folgendermaßen vorgehen:
  
- Legen Sie die Nachricht in eine interne Warteschlange, um auf die Übertragung zu warten, die Nachricht möglicherweise in den lokalen Speicher zu kopieren und zurückzugeben.
    
- Versuchen Sie, die eigentliche Übertragung auszuführen und nach Abschluss der Übertragung zurückzugeben, entweder erfolgreich oder nicht erfolgreich.
    
- Bestimmen Sie, ob die Nachricht nach der Überprüfung der betreffenden Ressource gesendet werden soll. Wenn die Ressource in diesem Fall kostenlos ist, kann der Anbieter die Ressource sperren, die Nachricht vorbereiten und übermitteln. Wenn die Ressource ausgelastet ist, kann der Anbieter die Nachricht vorbereiten und das Senden zu einem späteren Zeitpunkt zurückstellen.
    
Die bevorzugte Technik für die Nachrichtenübertragung hängt vom Transportanbieter und der erwarteten Anzahl von Prozessen ab, die um Systemressourcen konkurrieren. 
  
Während eines **SubmitMessage-Aufrufs** steuert der Transportanbieter die Übertragung von Nachrichtendaten aus dem Nachrichtenobjekt. Der Transportanbieter sollte der Nachricht jedoch einen Verweiswert zuweisen, auf den ein Zeiger in  _lpulMsgRef_ zurückgegeben wird, bevor Daten übertragen werden. Dies geschieht, da der MAPI-Spooler zu jedem Zeitpunkt während des Prozesses die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) aufrufen kann, wobei das NOTIFY_CANCEL_MESSAGE-Flag festgelegt ist, um dem Anbieter zu signalisieren, dass alle geöffneten Objekte freigegeben und die Nachrichtenübertragung beendet werden soll. 
  
Der Transportanbieter sollte keine nichttransmittablen Eigenschaften der Nachricht senden. Wenn eine solche Eigenschaft gefunden wird, sollte sie fortfahren, um die nächste Eigenschaft zu verarbeiten. Der Anbieter sollte alle Anstrengungen unternehmen, MAPI_P1 Empfängerinformationen nicht als Teil des übertragenen Nachrichteninhalts anzuzeigen. Der Anbieter sollte diese Empfängerinformationen nur zu Adressierungszwecken verwenden. MAPI_P1 Empfänger intern generierte Empfänger sind, die zum erneuten Senden von Nachrichten verwendet werden; sie sollten nicht übertragen werden. Verwenden Sie stattdessen die anderen Empfänger für die Übermittlung von Empfängerinformationen. Der Zweck dieser Anordnung besteht darin, erneut sendenden Empfängern zu ermöglichen, genau die gleiche Empfängertabelle wie die ursprünglichen Empfänger anzuzeigen.
  
Während eines **SubmitMessage-Aufrufs** verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und verarbeitet alle Anlagen. Diese Verarbeitung kann sehr viel Zeit in Anspruch nehmen. Transportanbieter können die [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) für den MAPI-Spooler während dieser Verarbeitung häufig aufrufen, um CPU-Zeit für andere Systemaufgaben freizugeben. 
  
Alle Nachrichtenempfänger sind in der Empfängertabelle der Nachricht sichtbar, die der MAPI-Spooler ursprünglich übergeben hat. Der Transportanbieter sollte nur die Empfänger verarbeiten, die er verarbeiten kann – basierend auf der Eintrags-ID, dem Adresstyp oder beiden – und deren **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft noch nicht auf TRUE festgelegt ist. Wenn **PR_RESPONSIBILITY** bereits auf TRUE festgelegt ist, hat ein anderer Transportanbieter diesen Empfänger behandelt. Wenn der Anbieter eine ausreichende Verarbeitung eines Empfängers abgeschlossen hat, um festzustellen, ob er Nachrichten für diesen Empfänger verarbeiten kann, sollte er die **eigenschaft PR_RESPONSIBILITY** des Empfängers in der übergebenen Nachricht auf TRUE festlegen. In der Regel trifft der Anbieter diese Entscheidung, nachdem die Nachrichtenübermittlung abgeschlossen ist. 
  
In der Regel wird der Transportanbieter erst dann von einem **SubmitMessage-Aufruf** zurückgegeben, wenn die Übertragung der Nachrichtendaten abgeschlossen ist. Wenn kein Fehler zurückgegeben wird, ist der nächste Aufruf des MAPI-Spoolers an den Anbieter ein Aufruf der [IXPLogon::EndMessage-Methode.](ixplogon-endmessage.md) 
  
Wenn **SubmitMessage** einen Fehler zurückgibt, gibt der MAPI-Spooler die Nachricht im Prozess frei, ohne Änderungen zu speichern. Wenn der Transportanbieter das Speichern von Nachrichtenänderungen erfordert, muss er die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die Nachricht vor der Rückgabe aufrufen. 
  
Bei Fehlern, die aufgrund von Transportproblemen auftreten, behält der MAPI-Spooler die Nachricht bei, verzögert jedoch die erneute Übermittlung der Nachricht an den Transportanbieter basierend auf dem in  _lpulReturnParm_ zurückgegebenen Wert. Der Transportanbieter muss diesen Wert eingeben, wenn der Rückgabewert von **SubmitMessage** MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR ist. Wenn eine schwerwiegende Fehlerbedingung auftritt, muss der Transportanbieter die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem flag NOTIFY_CRITICAL_ERROR aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

