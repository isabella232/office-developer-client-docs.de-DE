---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792886"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Betrifft**: Outlook 
  
Initiiert die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpMessage_
  
> [in] Ein Zeiger auf ein Objekt "Message" (für die eingehende Nachricht), die Lese-/Schreibberechtigung hat, die von der Adressbuchhierarchie zum Aufrufen und Bearbeiten dieser Nachricht verwendet wird. Dieses Objekt bleibt gültig bis, nachdem der Adressbuchhierarchie aus dem Aufruf von **IXPLogon::StartMessage**zurückgegeben.
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf ein Referenzwert, der die Nachricht zugewiesen. Die MAPI-Warteschlange initialisiert dieser Wert auf 1, bevor sie den Zeiger für den Transportanbieter zurückgibt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange die **IXPLogon::StartMessage** -Methode aufgerufen, um die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange zu initiieren. Vor Beginn der Adressbuchhierarchie mit der Meldung von _LpMessage_sollten sie eine Referenz zu Nachrichten im _LpulMsgRef_ -Parameter für die mögliche Verwendung durch einen Aufruf an die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode speichern. 
  
Während eines Anrufs **StartMessage** die MAPI-Warteschlange verarbeitet Methoden für Objekte, die während der Übertragung der Nachricht geöffnet, und es auch für die Verarbeitung von Anlagen. Diese Verarbeitung kann sehr lange dauern. Transportanbieter können die [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) Callback-Funktion für die MAPI-Warteschlange während diese Verarbeitung freizugebende CPU-Zeit für andere Systemaufgaben häufig aufrufen. 
  
Alle Empfänger in der Empfänger Tabelle, mit der der Adressbuchhierarchie für die Nachricht erstellt, müssen alle erforderliche reagieren auf Eigenschaften enthalten. Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger zur Darstellung von eines bestimmten Empfängers erstellen. Wenn der Anbieter einen Empfänger Eintrag, der Informationen enthält erzeugen kann, sollten sie dies tun. Beispielsweise sollte ein ein Transportdienstes genügend Informationen über eine Adressbuchanbieter Empfänger Format hat, dass er eine gültige Eintrags-ID für einen Empfänger für dieses Format erstellen kann, die Eintrags-ID erstellen.
  
Wenn alle Eigenschaften Nontransmittable empfangen werden, sollte der Adressbuchhierarchie nicht in die neue Nachricht gespeichert werden. Der Adressbuchhierarchie sollten jedoch alle Übertragungseinehit Eigenschaften speichern, die sie in der neuen Nachricht empfängt.
  
Wenn die eingehende Nachricht einen Übermittlungsbericht oder einen Unzustellbarkeitsbericht und der Adressbuchhierarchie nicht mit der [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode zum Generieren von Berichten aus der ursprünglichen Nachricht kann, sollte der Anbieter die Nachricht mit Auffüllen die entsprechenden Eigenschaften. Allerdings festlegen nicht der Adressbuchhierarchie die Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.
  
Um den entsprechenden MAPI-Nachrichtenspeicher nach der Verarbeitung die eingehende Nachricht speichern, ruft der Adressbuchhierarchie die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode. Wenn der Adressbuchhierarchie Nachrichten zum Übergeben an die Warteschlange MAPI nicht vorhanden ist, kann die eingehende Nachricht unterbrochen werden durch den Aufruf der **StartMessage** ohne einen Aufruf **SaveChanges**zurückgeben.
  
Alle Objekte, die während eines Anrufs **StartMessage** der Adressbuchhierarchie öffnet sollten vor der Rückgabe freigegeben werden. Der Anbieter sollte jedoch nicht Message-Objekts freigeben, die die MAPI-Warteschlange ursprünglich in der _LpMessage_ -Parameter übergeben. 
  
Wenn **StartMessage** einen Fehler zurückgibt, wird die Nachricht im Prozess wird aufgehoben, ohne dass Änderungen gespeichert und geht verloren. In diesem Fall sollte der Adressbuchhierarchie das Flag NOTIFY_CRITICAL_ERROR mit einem Aufruf der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode übergeben, und rufen Sie die [IXPLogon::Poll](ixplogon-poll.md) -Methode, um die MAPI-Warteschlange zu benachrichtigen, die dass er eine Bedingung Schwerwiegender Fehler ist. 
  
Weitere Informationen finden Sie unter [Interaktion mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

