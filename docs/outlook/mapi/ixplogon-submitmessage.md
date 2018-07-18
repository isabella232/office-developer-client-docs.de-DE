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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8a0b10596bdfdc1ea33f6d170ee1e021193d3788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792892"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**Betrifft**: Outlook 
  
Gibt an, dass die MAPI-Warteschlange eine Nachricht an der Adressbuchhierarchie übermittelt wurde.
  
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
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachricht gesendet wird. Das folgende Flag kann festgelegt werden:
    
BEGIN_DEFERRED 
  
> Die MAPI-Warteschlange ist der Aufruf eines Transportdienstes mit einer Meldung, die zuvor zurückgestellt wurde. Die Eintrags-ID der Nachricht ist identisch, wenn sie verschoben wurde. Die Nachricht wurde zurückgestellt, indem Sie die Eintrags-ID an die MAPI-Warteschlange mithilfe der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENTDEFERRED-Flag übergeben. 
    
 _lpMessage_
  
> [in] Ein Zeiger auf ein Objekt "Message" (für die Nachricht übermitteln), der über Lese-/Schreibberechtigung, verfügt der Adressbuchhierarchie aufrufen und Bearbeiten dieser Nachricht verwendet. Dieses Objekt bleibt gültig bis, nachdem der Adressbuchhierarchie aus einer nachfolgenden Aufruf der [IXPLogon::EndMessage](ixplogon-endmessage.md) -Methode zurückgibt. 
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf eine Variable, die in der der Adressbuchhierarchie den Verweiswert zurückgibt, den sie diese Meldung zugewiesen. Die MAPI-Warteschlange übergibt dieser Verweiswert nachfolgende Aufrufe für diese Nachricht. Die MAPI-Warteschlange initialisiert den Wert auf 0 vor der Rückgabe an den Transportanbieter.
    
 _lpulReturnParm_
  
> [out] Ein Zeiger auf eine Variable, die den Fehlerwert MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR **SubmitMessage**zurückgegebene entspricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
MAPI_E_BUSY 
  
> Der Adressbuchhierarchie kann nicht die Meldung, zu behandeln, da es einen anderen Vorgang ausgeführt wird. Ein Anbieter sollten dieser Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung aufgetreten ist und dass die MAPI-Warteschlange **EndMessage**nicht aufrufen soll. Die MAPI-Warteschlange wird den Anruf **SubmitMessage** einem späteren Zeitpunkt erneut versuchen. 
    
MAPI_E_CANCEL 
  
> Obwohl der Adressbuchhierarchie angefordert, dass die MAPI-Warteschlange die Nachricht in einem vorherigen Aufruf der **SpoolerNotify** erneut übermitteln, Bedingungen haben inzwischen geändert, und die Nachricht nicht erneut gesendet werden soll. Die MAPI-Warteschlange wird wechseln Sie auf einen anderen Suchbegriff behandelt. 
    
MAPI_E_NETWORK_ERROR 
  
> Ein Netzwerkfehler verhindert erfolgreichen Abschluss des Vorgangs. Der Parameter _LpulReturnParm_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen die MAPI-Warteschlange werden die Nachricht erneut übermittelt. 
    
MAPI_E_NOT_ME 
  
> Diese Meldung kann nicht der Adressbuchhierarchie behandeln. Die MAPI-Warteschlange sollte versuchen, an einen anderen Transportanbieter zu finden. Ein Anbieter sollten dieser Rückgabewert verwenden, um anzugeben, dass keine Verarbeitung aufgetreten ist und dass die MAPI-Warteschlange **EndMessage**nicht aufrufen soll.
    
MAPI_E_WAIT 
  
> Ein vorübergehendes Problem wird verhindert, dass der Adressbuchhierarchie Behandlung der Nachricht. Der Parameter _LpulReturnParm_ sollte auf die Anzahl der Sekunden festgelegt werden, die verstreichen die MAPI-Warteschlange werden die Nachricht erneut übermittelt. 
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange Ruft die **IXPLogon::SubmitMessage** -Methode auf, wenn es sich um eine Nachricht an der Adressbuchhierarchie übermittelt hat. Die Nachricht wird an der Adressbuchhierarchie übergeben, mit dem Parameter _LpMessage_ . 
  
Wenn der Anbieter die Nachricht anzunehmen bereit ist, muss einen Verweiswert zurück, mit dem Parameter _LpulMsgRef_ , Prozess der übergebene Objekt und den entsprechenden Wert (normalerweise S_OK) zurückgeben. Wenn der Anbieter nicht vorbereitete zum Verarbeiten der Weiterleitung ist, sollte es einen Fehlerwert zurückgegeben, und optional einen anderen MAPI-Wert zurück, in _LpulReturnParm_ , um anzugeben, wie lange die MAPI-Warteschlange warten soll, bevor die erneute Übermittlung der Nachricht. 
  
Eines Transportdienstes Implementierung dieser Methode kann die folgenden Aufgaben ausführen:
  
- Stellen Sie die Nachricht in einer internen Warteschlange, die für die Übertragung, kopieren die Nachricht möglicherweise an den lokalen Speicher warten und zurückzugeben.
    
- Versuchen Sie, führen Sie die tatsächliche Übertragung und zurückgeben, wenn die Übertragung erfolgreich oder nicht erfolgreich abgeschlossen wird.
    
- Bestimmen Sie, ob die Nachricht gesendet werden, nachdem die Beteiligten Ressource überprüft. In diesem Fall ist die Ressource frei, kann der Anbieter die Ressource zu sperren, Vorbereiten die Nachricht und senden sie Sie. Wenn die Ressource ausgelastet ist, kann der Anbieter vorbereiten die Nachricht und Senden an einem späteren Zeitpunkt verzögern.
    
Das bevorzugte Verfahren für die Nachrichtenübermittlung hängt davon ab, der Adressbuchhierarchie und der erwarteten Anzahl von Prozesse konkurrieren für Systemressourcen. 
  
Während eines Anrufs **SubmitMessage** steuert der Adressbuchhierarchie die Übertragung von Nachrichtendaten von Message-Objekts. Jedoch sollte der Adressbuchhierarchie einen Verweiswert der Nachricht zuweisen, der einen Zeiger in _LpulMsgRef_, wird vor der Weiterleitung von Daten. Darin wird, da jederzeit während des Aktivierungsvorgangs die MAPI-Warteschlange die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode mit dem NOTIFY_CANCEL_MESSAGE-Flag aufrufen kann so festgelegt, um dem Anbieter zu signalisieren, dass es sollten alle geöffneten Objekte freigeben und Beenden der Nachrichtenübermittlung. 
  
Der Transportdienst sollte keine Nontransmittable Eigenschaften der Nachricht senden. Wenn eine solche Eigenschaft gefunden wird, sollten sie wechseln Sie auf die nächste Eigenschaft verarbeitet. Der Anbieter sollte bemüht nicht für MAPI_P1 als Teil des Inhalts übertragene Nachricht Empfängerinformationen stellen. der Anbieter sollte diese Empfängerinformationen nur zum Umgang mit Zwecke verwenden. MAPI_P1 Empfänger sind intern generierten Empfänger, die für erneutes Senden von Nachrichten verwendet werden. Sie sollten nicht übertragen werden. Verwenden Sie stattdessen die anderen Empfänger für die Übertragung von Empfängerinformationen. Diese Anordnung dient gestatten erneut Empfänger genauen derselben Tabelle Empfänger als die ursprünglichen Empfänger zu sehen.
  
Während eines Anrufs **SubmitMessage** die MAPI-Warteschlange verarbeitet Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und alle Anlagen verarbeitet. Diese Verarbeitung kann sehr lange dauern. Transportanbieter können die [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) -Methode für die MAPI-Warteschlange während diese Verarbeitung freizugebende CPU-Zeit für andere Systemaufgaben häufig aufrufen. 
  
Alle Empfänger der Nachricht werden in der Tabelle Empfänger der Nachricht, die die MAPI-Warteschlange ursprünglich übergeben angezeigt. Der Transportdienst sollten nur die Empfänger, die es verarbeiten kann verarbeiten – basierend auf Eintrags-ID und/oder Adresstyp – und noch keine ihrer **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft auf TRUE festgelegt haben. Wenn **PR_RESPONSIBILITY** bereits auf "true" festgelegt ist, hat einen anderen Transportanbieter, die der Empfänger behandelt. Nach Abschluss der Anbieter über ausreichende Verarbeitung eines Empfängers, um festzustellen, ob sie Nachrichten für diesen Empfänger behandelt werden kann, sollte es des Empfängers **PR_RESPONSIBILITY** -Eigenschaft in der übergebenen Meldung auf TRUE festgelegt. In der Regel wird der Anbieter hierbei nach Abschluss der Nachrichtenübermittlung. 
  
Der Adressbuchhierarchie gibt in der Regel nicht von einem Aufruf **SubmitMessage** zurück, erst nach die Übertragung von Meldungsdaten Abschluss. Wenn kein Fehler zurückgegeben wird, ist der nächste Aufruf aus die MAPI-Warteschlange an den Anbieter einen Aufruf der [IXPLogon::EndMessage](ixplogon-endmessage.md) -Methode. 
  
Wenn **SubmitMessage** einen Fehler zurückgibt, gibt die MAPI-Warteschlange die Nachricht im Prozess frei, ohne Änderungen zu speichern. Benötigt der Adressbuchhierarchie Nachricht Änderungen gespeichert werden soll, muss er die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht vor der Rückgabe aufrufen. 
  
Bei Fehlern, die aufgrund von Transport Probleme auftreten, die MAPI-Warteschlange behält die Nachricht, aber sie verzögert erneute Übermittlung der Nachricht an der Adressbuchhierarchie basierend auf dem Wert in _LpulReturnParm_zurückgegeben. Wenn der Rückgabewert aus **SubmitMessage** MAPI_E_WAIT oder MAPI_E_NETWORK_ERROR ist, muss diesen Wert der Adressbuchhierarchie ausfüllen. Wenn eine Bedingung Schwerwiegender Fehler auftritt, muss der Adressbuchhierarchie die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_CRITICAL_ERROR-Flag aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

