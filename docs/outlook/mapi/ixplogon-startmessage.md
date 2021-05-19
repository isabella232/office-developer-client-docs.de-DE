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
  
> [in] Ein Zeiger auf ein Nachrichtenobjekt (das die eingehende Nachricht darstellt), das über Lese-/Schreibberechtigungen verfügt, die vom Transportanbieter verwendet werden, um auf diese Nachricht zu zugreifen und diese zu bearbeiten. Dieses Objekt bleibt gültig, bis der Transportanbieter vom Aufruf von **IXPLogon::StartMessage zurückkommt.**
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf einen Der Nachricht zugewiesenen Referenzwert. Der MAPI-Spooler initialisiert diesen Wert auf 1, bevor er den Zeiger an den Transportanbieter zurückgibt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::StartMessage-Methode** auf, um die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler zu initiieren. Bevor der Transportanbieter mit der Verwendung der Nachricht beginnt, auf die  _von lpMessage_ verwiesen wird, sollte er einen Nachrichtenverweis im  _lpulMsgRef-Parameter_ speichern, damit er durch einen Aufruf der [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) verwendet werden kann. 
  
Während eines **StartMessage-Aufrufs** verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet wurden, und verarbeitet auch Anlagen. Diese Verarbeitung kann sehr lange dauern. Transportanbieter können während dieser Verarbeitung häufig die [IMAPISupport::SpoolerYield-Rückruffunktion](imapisupport-spooleryield.md) für den MAPI-Spooler aufrufen, um die CPU-Zeit für andere Systemaufgaben frei zu geben. 
  
Alle Empfänger in der Empfängertabelle, die der Transportanbieter für die Nachricht erstellt, müssen alle erforderlichen Adressierungseigenschaften enthalten. Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger erstellen, der einen bestimmten Empfänger repräsentiert. Wenn der Anbieter jedoch einen Empfängereintrag erstellen kann, der weitere Informationen enthält, sollte er dies tun. Wenn ein Transportanbieter beispielsweise über genügend Informationen zum Empfängerformat eines Adressbuchanbieters verfügt, dass er einen gültigen Eintragsbezeichner für einen Empfänger für dieses Format erstellen kann, sollte er die Eintrags-ID erstellen.
  
Wenn nichttransmittable Eigenschaften empfangen werden, sollte der Transportanbieter sie nicht in der neuen Nachricht speichern. Der Transportanbieter sollte jedoch alle übertragungsbaren Eigenschaften speichern, die er in der neuen Nachricht erhält.
  
Wenn es sich bei der eingehenden Nachricht um einen Zustellungsbericht oder einen Nicht-Zustellungsbericht handelt und der Transportanbieter die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) nicht verwenden kann, um den Bericht aus der ursprünglichen Nachricht zu generieren, sollte der Anbieter die Nachricht selbst mit den entsprechenden Eigenschaften auffüllen. Der Transportanbieter kann jedoch die Eigenschaft PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) der Nachricht nicht festlegen.
  
Um die eingehende Nachricht nach der Verarbeitung im entsprechenden MAPI-Nachrichtenspeicher zu speichern, ruft der Transportanbieter die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) auf. Wenn der Transportanbieter über keine Nachrichten verfügt, die an den MAPI-Spooler übergeben werden sollen, kann er die eingehende Nachricht beenden, indem er vom **StartMessage-Anruf** ohne **SaveChanges zurückkehrt.**
  
Alle Objekte, die der Transportanbieter während eines **StartMessage-Aufrufs** öffnet, sollten vor der Rückgabe freigegeben werden. Der Anbieter sollte jedoch das Message-Objekt nicht los, das der MAPI-Spooler ursprünglich im  _lpMessage-Parameter übergeben_ hat. 
  
Wenn **StartMessage** einen Fehler zurückgibt, wird die In-Process-Nachricht ohne gespeicherte Änderungen freigegeben und geht verloren. In diesem Fall sollte der Transportanbieter das NOTIFY_CRITICAL_ERROR-Flag mit einem Aufruf der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) übergeben und die [IXPLogon::P oll-Methode](ixplogon-poll.md) aufrufen, um den MAPI-Spooler zu benachrichtigen, dass er sich in einem schwerwiegenden Fehlerzustand befindet. 
  
Weitere Informationen finden Sie unter [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

