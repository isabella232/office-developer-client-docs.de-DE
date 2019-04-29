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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427605"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler.
  
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
  
> in Ein Zeiger auf ein Nachrichtenobjekt (das die eingehende Nachricht darstellt) mit Lese-/Schreibzugriff, das vom Transportanbieter zum zugreifen und Bearbeiten dieser Nachricht verwendet wird. Dieses Objekt bleibt gültig, bis der Transportanbieter vom Aufruf an **IXPLogon:: StartMessage**zurückkehrt.
    
 _lpulMsgRef_
  
> Out Ein Zeiger auf einen Verweiswert, der der Nachricht zugewiesen ist. Der MAPI-Spooler initialisiert diesen Wert mit 1, bevor er den Zeiger an den Transportanbieter zurückgibt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IXPLogon:: StartMessage** -Methode auf, um die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler zu initiieren. Bevor der Transportanbieter mit der Verwendung der Nachricht beginnt, auf die von _lpMessage_verwiesen wird, sollte ein Nachrichtenverweis im _lpulMsgRef_ -Parameter gespeichert werden, damit Sie von einem Aufruf der [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode verwendet werden kann. 
  
Während eines **StartMessage** -Aufrufs verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und verarbeitet auch Anlagen. Diese Verarbeitung kann sehr viel Zeit in Anspruch nehmen. Transport Anbieter können die [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) -Rückruffunktion für den MAPI-Spooler während dieser Verarbeitung häufig aufrufen, um die CPU-Zeit für andere Systemaufgaben zu veröffentlichen. 
  
Alle Empfänger in der Empfängertabelle, die der Transportanbieter für die Nachricht erstellt, müssen alle erforderlichen Adressierungs Eigenschaften enthalten. Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger erstellen, um einen bestimmten Empfänger darzustellen. Wenn der Anbieter jedoch einen Empfängereintrag mit weiteren Informationen erstellen kann, sollte dies der Fall sein. Wenn beispielsweise ein Transportanbieter über genügend Informationen zum Empfänger Format des Adressbuch Anbieters verfügt, dass er eine gültige Eintrags-ID für einen Empfänger für dieses Format erstellen kann, sollte er die Eintrags-ID erstellen.
  
Wenn nicht übertragbare Eigenschaften empfangen werden, sollte der Transportanbieter diese nicht in der neuen Nachricht speichern. Der Transportanbieter sollte jedoch alle übertragenen Eigenschaften speichern, die er in der neuen Nachricht empfängt.
  
Wenn die eingehende Nachricht ein zugestellter Bericht oder ein Unzustellbarkeitsbericht ist und der Transportanbieter die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode nicht verwenden kann, um den Bericht aus der ursprünglichen Nachricht zu generieren, sollte der Anbieter die Nachricht selbst mit die entsprechenden Eigenschaften. Der Transportanbieter kann jedoch die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft der Nachricht nicht festlegen.
  
Wenn die eingehende Nachricht nach der Verarbeitung im entsprechenden MAPI-Nachrichtenspeicher gespeichert werden soll, ruft der Transportanbieter die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode auf. Wenn der Transportanbieter keine Nachrichten an den MAPI-Spooler übergibt, kann er die eingehende Nachricht beenden, indem er vom **StartMessage** -Aufruf zurückkehrt ****, ohne SaveChanges zu aufrufen.
  
Alle Objekte, die der Transportanbieter während eines **StartMessage** -Aufrufs geöffnet hat, sollten vor der Rückgabe freigegeben werden. Der Anbieter sollte jedoch das Message-Objekt, das der MAPI-Spooler ursprünglich im _lpMessage_ -Parameter übergeben hat, nicht freigeben. 
  
Wenn **StartMessage** einen Fehler zurückgibt, wird die Nachricht in Process ohne gespeicherte Änderungen freigegeben und geht verloren. In diesem Fall sollte der Transportanbieter das NOTIFY_CRITICAL_ERROR-Flag mit einem Aufruf an die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode weiterleiten und die [IXPLogon::P oll](ixplogon-poll.md) -Methode aufrufen, um die MAPI-Warteschlange zu benachrichtigen, dass Sie sich in einem schwerwiegenden Fehlerzustand befindet. 
  
Weitere Informationen finden Sie unter [interagieren mit dem MAPI](interacting-with-the-mapi-spooler.md)-Spooler. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

