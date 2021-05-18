---
title: IPersistMessageInitNeu
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
  
> [in] Ein Zeiger auf die Nachrichtenwebsite, die das Formular zum Arbeiten mit der Nachricht im Viewer verwendet.
    
 _pMessage_
  
> [in] Ein Zeiger auf die neue Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die neue Nachricht wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IPersistMessage::InitNew-Methode** auf, wenn der Benutzer eine neue Nachricht schreibt, die zu einer Nachrichtenklasse gehört, die vom Formular verarbeitet wird. Wenn das Formularobjekt über einen gültigen Benutzeroberflächenzeiger verfügt, sollte die Benutzeroberfläche für das Nachrichtenobjekt angezeigt werden. 
  
 **InitNew** sollte nicht aufgerufen werden, wenn sich Ihr Formular in einem beliebigen Zustand befindet, mit Ausnahme des [Status "Nicht initialisiert".](uninitialized-state.md) Wenn sich das Formular in einem der anderen Zustände befindet, wenn **InitNew** aufgerufen wird, geben Sie E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

In der Regel werden Nachrichten mit nicht gespeicherten Eigenschaften als geändert gekennzeichnet, sodass der Client ein Dialogfeld anzeigen kann, in dem der Benutzer gefragt wird, ob diese Eigenschaften gespeichert werden sollen. Wenn der Benutzer angibt, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren Sie die Nachricht als sauber, und beenden Sie sie normal.
  
Wenn die Verarbeitung ihrer neu initialisierten Nachrichten jedoch das Festlegen einer oder mehrerer berechneter Eigenschaften umfasst und es wichtig ist, dass diese Eigenschaften gespeichert werden, markieren Sie die Nachrichten nicht als geändert. Da berechnete Eigenschaften für Benutzer nicht sichtbar sein sollten, sollte kein Dialogfeld angezeigt werden.
  
Wenn Ihr Formular einen Verweis auf eine andere aktive Nachrichtenwebsite als die an **InitNew** übergebene enthält, geben Sie die ursprüngliche Website frei, da sie nicht mehr verwendet wird. Store die Zeiger auf die Nachrichtenwebsite und -nachricht von den _Parametern pMessageSite_ und _pMessage_ aus und rufen die [IUnknown::AddRef-Methoden](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) beider Objekte auf, um ihre Referenzanzahl zu erhöhen. 
  
Legen Sie die **eigenschaften PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) für die neue Nachricht auf eine für Ihre Nachrichtenklasse geeignete Eigenschaft. Viele Nachrichtenklassen legen z. **B.** PR_MESSAGE_FLAGS auf MSGFLAG_UNSENT neuen Nachrichten festgelegt. 
  
Bevor Sie das Formular zurückgeben, müssen Sie das Formular in den [Status Normal überwechseln,](normal-state.md) wenn keine Fehler aufgetreten sind. Senden Sie eine neue Nachrichtenbenachrichtigung an alle registrierten Viewer, indem Sie ihre [IMAPIViewAdviseSink::OnNewMessage-Methoden](imapiviewadvisesink-onnewmessage.md) aufrufen und S_OK. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem Sie einen erfolgreichen Aufruf von **InitNew** vorgenommen haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine anderen Eigenschaften für das Formular festgelegt wurden:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Weitere Informationen zu den Zuständen von Formularen finden Sie unter [Formularzustände](form-states.md). Weitere Informationen zum Initialisieren von Speicherobjekten finden Sie unter [der IPersistStorage::InitNew-Methode.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

