---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 88a49c09f7f4e2678265fae20dddc8833716a2e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630425"
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
  
> [in] Ein Zeiger auf die Nachrichtenwebsite, die das Formular verwendet, um mit der Nachricht im Viewer zu arbeiten.
    
 _pMessage_
  
> [in] Ein Zeiger auf die neue Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die neue Nachricht wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Bemerkungen

Formularviewer rufen die **IPersistMessage::InitNew-Methode** auf, wenn der Benutzer eine neue Nachricht schreibt, die zu einer Nachrichtenklasse gehört, die das Formular verarbeitet. Wenn das Formularobjekt über einen gültigen Benutzeroberflächenzeiger verfügt, sollte die Benutzeroberfläche für das Nachrichtenobjekt angezeigt werden. 
  
 **InitNew** sollte nicht aufgerufen werden, wenn sich das Formular in einem Zustand mit Ausnahme des Status ["Nicht initialisiert"](uninitialized-state.md) befindet. Wenn sich das Formular beim Aufrufen von **InitNew** in einem der anderen Zustände befindet, geben Sie E_UNEXPECTED zurück. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

In der Regel werden Nachrichten mit nicht gespeicherten Eigenschaften als geändert markiert, sodass der Client ein Dialogfeld anzeigen kann, in dem der Benutzer gefragt wird, ob diese Eigenschaften gespeichert werden sollen. Wenn der Benutzer angibt, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren Sie die Nachricht als sauber, und beenden Sie sie normal.
  
Wenn die Verarbeitung ihrer neu initialisierten Nachrichten jedoch das Festlegen einer oder mehrerer berechneter Eigenschaften umfasst und es wichtig ist, dass diese Eigenschaften gespeichert werden, markieren Sie die Nachrichten nicht als geändert. Da berechnete Eigenschaften für Benutzer unsichtbar sein sollen, sollte kein Dialogfeld angezeigt werden.
  
Wenn Ihr Formular einen Verweis auf eine aktive Nachrichtenwebsite hat, die nicht der an **InitNew** übergeben wird, geben Sie die ursprüngliche Website frei, da sie nicht mehr verwendet wird. Store die Zeiger auf die Nachrichtenwebsite und die Nachricht aus den _Parametern pMessageSite_ und _pMessage,_ und rufen Sie die [IUnknown::AddRef-Methoden](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) beider Objekte auf, um deren Verweisanzahl zu erhöhen. 
  
Legen Sie die Eigenschaften **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) für die neue Nachricht auf eine für Ihre Nachrichtenklasse geeignete Eigenschaft fest. Viele Nachrichtenklassen legen beispielsweise **PR_MESSAGE_FLAGS** auf MSGFLAG_UNSENT für neue Nachrichten fest. 
  
Bevor Sie zurückkehren, wechseln Sie das Formular in den [Standardzustand,](normal-state.md) wenn keine Fehler aufgetreten sind. Senden Sie eine neue Nachrichtenbenachrichtigung an alle registrierten Benutzer, indem Sie ihre [IMAPIViewAdviseSink::OnNewMessage-Methoden](imapiviewadvisesink-onnewmessage.md) aufrufen und S_OK zurückgeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem Sie **InitNew** erfolgreich aufgerufen haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine anderen Eigenschaften für das Formular festgelegt wurden:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Weitere Informationen zu den Zuständen von Formularen finden Sie unter ["Formularstatus".](form-states.md) Weitere Informationen zur Initialisierung von Speicherobjekten finden Sie unter der [IPersistStorage::InitNew-Methode.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

