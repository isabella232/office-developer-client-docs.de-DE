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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e237e73f59fa691821dcb55b59f5d17518451797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792723"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Betrifft**: Outlook 
  
Initialisiert eine neue Nachricht an.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameter

 _pMessageSite_
  
> [in] Ein Zeiger auf die Nachricht-Website, die das Formular verwendet wird, um die Nachricht im Viewer entwickelt.
    
 _pMessage_
  
> [in] Ein Zeiger auf die neue Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die neue Nachricht wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen die **IPersistMessage::InitNew** -Methode auf, wenn der Benutzer eine neue Nachricht verfasst, zu der eine Nachrichtenklasse gehört, der das Formular behandelt. Wenn das Form-Objekt einen gültigen Benutzernamen Schnittstellenzeiger aufweist, sollte die Benutzeroberfläche für das Objekt "Message" angezeigt. 
  
 **InitNew** sollte nicht aufgerufen werden, wenn das Formular in einen beliebigen Zustand außer den Status [nicht initialisiert](uninitialized-state.md) wird. Wenn das Formular eines der anderen Status ist **InitNew** aufgerufen wird, zurückgeben Sie E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

In der Regel werden Nachrichten, die Eigenschaften nicht gespeicherte haben als geändert markiert, sodass der Client ein Dialogfeld angezeigt werden kann, die der Benutzer aufgefordert wird, ob diese Eigenschaften gespeichert werden soll. Wenn der Benutzer gibt an, dass eine Nachricht gespeichert werden soll, speichern Sie die Daten, markieren der Nachricht als clean und normal beenden.
  
Jedoch wenn Verarbeitung für Ihre neu initialisierten Nachrichten umfasst eine festlegen oder Eigenschaften berechnete, und es ist wichtig für diese Eigenschaften gespeichert werden soll, führen Sie nicht die Nachrichten als geändert zu markieren. Da berechnete Eigenschaften für Benutzer nicht sichtbar sein soll, sollte das Dialogfeld nicht angezeigt werden.
  
Wenn Ihr Formular einen Verweis auf eine aktive Nachricht Website als derjenigen, die in **InitNew**übergeben wird, lassen Sie die ursprüngliche Website, da sie nicht mehr verwendet werden. Der Zeiger auf die Nachricht-Website und die Nachricht der Parameter _pMessageSite_ und _pMessage_ gespeichert, und rufen beide Objekte [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) Methoden, um ihre Referenzzähler erhöhen. 
  
Legen Sie die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) und **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaften für die neue Nachricht in einen passenden für Ihre Nachrichtenklasse ein. Viele Nachrichtenklassen, legen Sie beispielsweise **PR_MESSAGE_FLAGS** auf MSGFLAG_UNSENT für neue Nachrichten. 
  
Vor der Rückgabe, Übergang des Formulars auf den [normalen](normal-state.md) Status, wenn keine Fehler aufgetreten. Senden Sie eine neue Benachrichtigung an alle registrierten Viewer durch ihre [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methoden aufrufen, und geben Sie S_OK zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nachdem Sie einen erfolgreichen Aufruf von **InitNew**vorgenommen haben, können Sie davon ausgehen, dass die folgenden erforderlichen Eigenschaften und keine andere, für das Formular festgelegt wurden:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Weitere Informationen über die Zustände von Formularen finden Sie unter [Formular Zustände](form-states.md). Weitere Informationen dazu, wie Speicherobjekte initialisiert werden finden Sie unter der [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

