---
title: Senden von Nachrichten Transport Anbieter Aufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 431e3d2f66616db2c586b76387a8521832ed985f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426548"
---
# <a name="sending-messages-transport-provider-tasks"></a>Senden von Nachrichten: Aufgaben des Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **Eine Nachricht Anbietern f�r die Daten�bertragung �bermitteln**
  
- Legen Sie die eigenschaft **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) der Nachricht auf TRUE festgelegt, nachdem der Transportanbieter die Nachricht gesendet oder versucht hat, die Nachricht zu senden. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Wenn die Nachricht erfolgreich gesendet wird und die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, erstellen Sie eine [ADRLIST-Struktur](adrlist.md) mit den erfolgreichen Empfängern, legen Sie die **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))-Eigenschaft für jeden Wert ein, und rufen Sie **StatusRecips** auf, um einen Zustellungsbericht zu generieren. For more information about creating delivery and non-delivery reports, see the following topics: [MAPI-Berichtnachrichten](mapi-report-messages.md), [Erforderliche Bericht Nachrichteneigenschaften](required-report-message-properties.md), [Optional Bericht Nachrichteneigenschaften](optional-report-message-properties.md), and [�bermittlungsberichte Nachricht senden](sending-message-delivery-reports.md).
    
- Legen Sie die Nachricht **PR_SENDER** Gruppe von Eigenschaften auf die Identit�t des Benutzers, der angemeldet hat. Diese Gruppe umfasst: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) und **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Legen Sie die Nachrichteneigenschaften **PR_SENT_REPRESENTING**, wenn m�glich, um entweder die Identit�t des Benutzers, der angemeldet hat oder auf eine g�ltige Delegaten Identit�t. Die Eigenschaften **PR_SENT_REPRESENTING** dienen zum Implementieren, das Senden von Nachrichten von einem Benutzer im Auftrag eines anderen Benutzers. Anbietern f�r die Daten�bertragung, die diese Eigenschaften nicht unterst�tzen, sollten sie f�r ausgehende Nachrichten ignorieren. 
    
- Legen Sie die eigenschaft **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) der Nachricht so ein, dass angegeben wird, wann der Client [IMessage::SubmitMessage aufgerufen hat.](imessage-submitmessage.md)
    
- Legen Sie die PR_PROVIDER_SUBMIT_TIME **(** [PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) -Eigenschaft der Nachricht fest, um das Datum und die Uhrzeit anzugeben, zu der der Nachrichtenspeicheranbieter die Nachricht als gesendet markiert hat. 
    
Wenn eine Nachricht an eine Vielzahl von Empf�ngern mit verschiedenen Messagingsystemen gesendet wird, wird jede �bertragene Kopie eine anderen Absenderidentit�t haben. 
  
Der Transportdienst oder eng gekoppelten Nachrichtenspeicher und Transport ist auch verantwortlich f�r die Festlegung von Absender und Antwort-an-Informationen. Informationen zum Ersteller ist in den Eigenschaften des **PR_ORIGINATOR** und Antwort-an-Informationen in den Eigenschaften des PR_REPLY gespeichert. Der Client kann diese Eigenschaften festgelegt. jedoch ist der Adressbuchhierarchie zu ignorieren und �berschreiben von Einstellungen f�r den Client zul�ssig. 
  

