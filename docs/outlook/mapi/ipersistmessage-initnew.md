---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317150"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert eine neue Nachricht.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameter

 _pMessageSite_
  
> in Ein Zeiger auf die Nachrichtenwebsite, die das Formular für die Arbeit mit der Nachricht im Viewer verwendet.
    
 _pMessage_
  
> in Ein Zeiger auf die neue Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die neue Nachricht wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IPersistMessage:: InitNew** -Methode auf, wenn der Benutzer eine neue Nachricht schreibt, die zu einer Nachrichtenklasse gehört, die vom Formular verarbeitet wird. Wenn das Form-Objekt einen gültigen Benutzeroberflächen Zeiger aufweist, sollte die Benutzeroberfläche für das Message-Objekt angezeigt werden. 
  
 **InitNew** sollte nicht aufgerufen werden, wenn sich das Formular in einem beliebigen Zustand [](uninitialized-state.md) mit Ausnahme des nicht initialisierten Zustands befindet. Wenn sich das Formular in einem der anderen Zustände befindet, wenn **InitNew** aufgerufen wird, geben Sie E_UNEXPECTED zurück. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

In der Regel werden Nachrichten mit nicht gespeicherten Eigenschaften als geändert gekennzeichnet, sodass der Client ein Dialogfeld anzeigen kann, in dem der Benutzer gefragt wird, ob diese Eigenschaften gespeichert werden sollen. Wenn der Benutzer angibt, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren Sie die Nachricht als sauber, und beenden Sie sie normal.
  
Wenn die Verarbeitung für Ihre neu initialisierten Nachrichten jedoch eine oder mehrere berechnete Eigenschaften festlegt und es wichtig ist, diese Eigenschaften zu speichern, markieren Sie die Nachrichten nicht als geändert. Da berechnete Eigenschaften für Benutzer unsichtbar sein sollen, sollte kein Dialogfeld angezeigt werden.
  
Wenn das Formular einen Verweis auf eine aktive Nachrichtenwebsite hat, die nicht an **InitNew**übergeben wird, geben Sie die ursprüngliche Website frei, da Sie nicht mehr verwendet wird. Speichern Sie die Zeiger auf den Nachrichten Standort und die Nachricht aus den Parametern _pMessageSite_ und _pMessage_ , und rufen Sie die Methoden [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Objekte auf, um Ihre Verweisanzahl zu erhöhen. 
  
Legen Sie die Eigenschaften **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md)) für die neue Nachricht auf einen für Ihre Nachrichtenklasse geeigneten Wert fest. Viele Nachrichtenklassen legen **PR_MESSAGE_FLAGS** für neue Nachrichten auf MSGFLAG_UNSENT fest. 
  
Wechseln Sie vor dem zurückgeben das Formular in den [Normal](normal-state.md) Zustand, wenn keine Fehler aufgetreten sind. Senden Sie eine neue Nachrichten Benachrichtigung an alle registrierten Viewer, indem Sie Ihre [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen und S_OK zurückgeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem Sie einen erfolgreichen Aufruf an **InitNew**durchgeführt haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine anderen für das Formular festgelegt wurden:
  
 **PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([Pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([Pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))
  
Weitere Informationen zu den Status von Formularen finden Sie unter [Formular Status](form-states.md). Weitere Informationen zur Initialisierung von Speicherobjekten finden Sie unter der [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

