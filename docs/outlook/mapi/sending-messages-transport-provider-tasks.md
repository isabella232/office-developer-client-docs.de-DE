---
title: Senden von Nachrichten Transport Anbieter Aufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa25f575e55eb3d0446148d75de314a8883a4170
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591178"
---
# <a name="sending-messages-transport-provider-tasks"></a>Senden von Nachrichten: Transportanbieteraufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **Eine Nachricht Anbietern f�r die Daten�bertragung �bermitteln**
  
- Legen Sie die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) der Nachricht auf TRUE fest, nachdem der Transportanbieter die Nachricht gesendet oder versucht hat, die Nachricht zu senden. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Wenn die Nachricht erfolgreich gesendet wurde und die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist, erstellen Sie eine [ADRLIST-Struktur](adrlist.md) mit den erfolgreichen Empfängern, legen Sie die **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) -Eigenschaft für jeden fest, und rufen **Sie StatusRecips** auf, um einen Übermittlungsbericht zu generieren. For more information about creating delivery and non-delivery reports, see the following topics: [MAPI-Berichtnachrichten](mapi-report-messages.md), [Erforderliche Bericht Nachrichteneigenschaften](required-report-message-properties.md), [Optional Bericht Nachrichteneigenschaften](optional-report-message-properties.md), and [�bermittlungsberichte Nachricht senden](sending-message-delivery-reports.md).
    
- Legen Sie die Nachricht **PR_SENDER** Gruppe von Eigenschaften auf die Identit�t des Benutzers, der angemeldet hat. Diese Gruppe umfasst: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) und **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Legen Sie die Nachrichteneigenschaften **PR_SENT_REPRESENTING**, wenn m�glich, um entweder die Identit�t des Benutzers, der angemeldet hat oder auf eine g�ltige Delegaten Identit�t. Die Eigenschaften **PR_SENT_REPRESENTING** dienen zum Implementieren, das Senden von Nachrichten von einem Benutzer im Auftrag eines anderen Benutzers. Anbietern f�r die Daten�bertragung, die diese Eigenschaften nicht unterst�tzen, sollten sie f�r ausgehende Nachrichten ignorieren. 
    
- Legen Sie die **eigenschaft PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) der Nachricht fest, um anzugeben, wann der Client [IMessage::SubmitMessage](imessage-submitmessage.md)aufgerufen hat.
    
- Legen Sie die **Eigenschaft PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) der Nachricht fest, um das Datum und die Uhrzeit anzugeben, zu der die Nachricht vom Nachrichtenspeicheranbieter als gesendet markiert wurde. 
    
Wenn eine Nachricht an eine Vielzahl von Empf�ngern mit verschiedenen Messagingsystemen gesendet wird, wird jede �bertragene Kopie eine anderen Absenderidentit�t haben. 
  
Der Transportdienst oder eng gekoppelten Nachrichtenspeicher und Transport ist auch verantwortlich f�r die Festlegung von Absender und Antwort-an-Informationen. Informationen zum Ersteller ist in den Eigenschaften des **PR_ORIGINATOR** und Antwort-an-Informationen in den Eigenschaften des PR_REPLY gespeichert. Der Client kann diese Eigenschaften festgelegt. jedoch ist der Adressbuchhierarchie zu ignorieren und �berschreiben von Einstellungen f�r den Client zul�ssig. 
  

