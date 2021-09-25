---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c3ce2ce255ad3469b158e57a39013e06eb3d75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595938"
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
  
> [in] Ein Zeiger auf ein Nachrichtenobjekt (das die eingehende Nachricht darstellt), das über Lese-/Schreibberechtigungen verfügt, die vom Transportanbieter verwendet werden, um auf diese Nachricht zuzugreifen und sie zu bearbeiten. Dieses Objekt bleibt gültig, bis der Transportanbieter vom Aufruf von **IXPLogon::StartMessage** zurückgegeben wird.
    
 _lpulMsgRef_
  
> [out] Ein Zeiger auf einen Verweiswert, der der Nachricht zugewiesen ist. Der MAPI-Spooler initialisiert diesen Wert auf 1, bevor der Zeiger an den Transportanbieter zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::StartMessage-Methode** auf, um die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler zu initiieren. Bevor der Transportanbieter beginnt, die Nachricht zu verwenden, auf die  _lpMessage_ verweist, sollte er einen Nachrichtenverweis im  _lpulMsgRef-Parameter_ speichern, damit er von einem Aufruf der [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) verwendet werden kann. 
  
Während eines **StartMessage-Aufrufs** verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet wurden, und verarbeitet auch alle Anlagen. Diese Verarbeitung kann sehr viel Zeit in Anspruch nehmen. Transportanbieter können während dieser Verarbeitung häufig die [IMAPISupport::SpoolerYield-Rückruffunktion](imapisupport-spooleryield.md) für den MAPI-Spooler aufrufen, um CPU-Zeit für andere Systemaufgaben freizugeben. 
  
Alle Empfänger in der Empfängertabelle, die der Transportanbieter für die Nachricht erstellt, müssen alle erforderlichen Adressierungseigenschaften enthalten. Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger erstellen, der einen bestimmten Empfänger darstellt. Wenn der Anbieter jedoch einen Empfängereintrag erstellen kann, der weitere Informationen enthält, sollte dies der Fall sein. Wenn ein Transportanbieter beispielsweise über genügend Informationen zum Empfängerformat eines Adressbuchanbieters verfügt, um einen gültigen Eintragsbezeichner für einen Empfänger für dieses Format erstellen zu können, sollte er den Eintragsbezeichner erstellen.
  
Wenn nicht übermittbare Eigenschaften empfangen werden, sollte der Transportanbieter sie nicht in der neuen Nachricht speichern. Der Transportanbieter sollte jedoch alle übertragenen Eigenschaften speichern, die er in der neuen Nachricht empfängt.
  
Wenn es sich bei der eingehenden Nachricht um einen Übermittlungsbericht oder einen Unzustellbarkeitsbericht handelt und der Transportanbieter die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) nicht verwenden kann, um den Bericht aus der ursprünglichen Nachricht zu generieren, sollte der Anbieter die Nachricht selbst mit den entsprechenden Eigenschaften auffüllen. Der Transportanbieter kann jedoch die **Eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der Nachricht nicht festlegen.
  
Zum Speichern der eingehenden Nachricht im entsprechenden MAPI-Nachrichtenspeicher nach der Verarbeitung ruft der Transportanbieter die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) auf. Wenn der Transportanbieter keine Nachrichten hat, die an den MAPI-Spooler übergeben werden müssen, kann er die eingehende Nachricht beenden, indem er vom **StartMessage-Aufruf** zurückgibt, ohne **SaveChanges** aufzurufen.
  
Alle Objekte, die der Transportanbieter während eines **StartMessage-Aufrufs** öffnet, sollten vor der Rückgabe freigegeben werden. Der Anbieter sollte jedoch nicht das Nachrichtenobjekt freigeben, das der MAPI-Spooler ursprünglich im  _lpMessage-Parameter_ übergeben hat. 
  
Wenn **StartMessage** einen Fehler zurückgibt, wird die nachricht im Prozess freigegeben, ohne dass Änderungen gespeichert wurden, und geht verloren. In diesem Fall sollte der Transportanbieter das NOTIFY_CRITICAL_ERROR Flag mit einem Aufruf der [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) übergeben und die [IXPLogon::P oll-Methode](ixplogon-poll.md) aufrufen, um den MAPI-Spooler zu benachrichtigen, dass er sich in einer schwerwiegenden Fehlerbedingung befindet. 
  
Weitere Informationen finden Sie unter [Interagieren mit dem MAPI-Spooler.](interacting-with-the-mapi-spooler.md) 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

