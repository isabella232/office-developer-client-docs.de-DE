---
title: Stellvertretungszugriff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427262"
---
# <a name="delegate-access"></a>Stellvertretungszugriff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Delegieren des Zugriffs bezieht sich auf die M�glichkeit des Benutzers als anderer Benutzer eine Nachricht senden oder Empfangen einer Nachricht an einen anderen Benutzer. Delegieren des Zugriffs ist ein Service Provider unabh�ngigen Feature von MAPI, das Transportanbieter unterst�tzt werden k�nnen, falls gew�nscht. Jedoch ist kein Anbieter dazu erforderlich. Delegieren des Zugriffs ist hilfreich, wenn es f�r einen Benutzer als Nachrichten senden oder Filtern eingehende Nachrichten auf, wenn ein Benutzer Nachrichtenspeicher eines anderen Benutzers zugreifen muss oder eines anderen Benutzers erforderlich ist. Bevor Sie eine Verbindung mit einem anderen Benutzerspeicher Stellvertretungsbenutzers zulassen, muss der Nachricht Speicheranbieter �berpr�fen, ob Stellvertretungsbenutzers die entsprechende Autorit�t verf�gt. 
  
Es gibt zwei Gruppen von Eigenschaften, die zur Unterst�tzung von Zugriffsrechten f�r Stellvertretung verwendet werden:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** ([Pidtagsentrepresentingaddresstype (](pidtagsentrepresentingaddresstype-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([Pidtagsentrepresentingemailaddress (](pidtagsentrepresentingemailaddress-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_ENTRYID** ([Pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** ([Pidtagsentrepresentingsearchkey (](pidtagsentrepresentingsearchkey-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** ([Pidtagreceivedrepresentingaddresstype (](pidtagreceivedrepresentingaddresstype-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([Pidtagreceivedrepresentingemailaddress (](pidtagreceivedrepresentingemailaddress-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** ([Pidtagreceivedrepresentingsearchkey (](pidtagreceivedrepresentingsearchkey-canonical-property.md)) 
  
F�r ausgehende Nachrichten den **PR_SENT_REPRESENTING** Eigenschaften identifiziert des messaging-Benutzers, der als Absender fungieren soll. Clients k�nnen diese Eigenschaften als Option festlegen. Wenn die **PR_SENT_REPRESENTING** Zeitpunkt nicht festgelegt werden des Anbieters Verantwortung zusammen mit den Eigenschaften **PR_SENDER** festgelegt ist, die Nachricht erreicht eine Adressbuchhierarchie Delegieren des Zugriffs, unterst�tzt. 
  
F�r eingehende Nachrichten identifizieren die **PR_RCVD_REPRESENTING** -Eigenschaften des Benutzers, der als Empf�nger fungieren soll. Zum �bermitteln von Delegatnachrichten Anbietern f�r die Daten�bertragung m�ssen die **PR_RCVD_REPRESENTING** und die **PR_RECEIVED_BY** Eigenschaften festlegen. Empfangen einer Nachricht Delegaten Clients sollten die Werte der Eigenschaften **PR_SENT_REPRESENTING** in die entsprechenden Eigenschaften **PR_RCVD_REPRESENTING** kopieren. 
  
Angenommen Sie, dass John Sallys Nachrichten erh�lt, w�hrend Sally im Urlaub ist. Die Eigenschaften **PR_RCVD_REPRESENTING** identifizieren John als Stellvertretung Empf�nger. Wenn John eine Antwort auf eine Nachricht, die er erhalten hat f�r Sally sendet, identifizieren Sie die Nachrichteneigenschaften **PR_SENDER** John als Absender. Da John Sally darstellt, von den Eigenschaften **PR_SENT_REPRESENTING** Sally identifiziert. 
  
Transport-Anbieter f�r die Verarbeitung eingehender Delegatnachrichten in der Regel diese Nachrichten als der durch die Eigenschaften **PR_SENT_REPRESENTING** identifizierte messaging Benutzer und nicht als der durch die Eigenschaften **PR_SENDER** identifizierte Benutzer �bermitteln soll. Die Ausnahme zu dieser Regel ist, wenn es erforderlich ist, Berechtigungen und Transport Zugriffsarten �bereinstimmen. In diesem Fall kann eine Adressbuchhierarchie eine sendende Identit�t ausw�hlen. 
  
Wenn die **PR_SENT_REPRESENTING** -Eigenschaften f�r eine eingehende Nachricht Stellvertretung nicht verf�gbar sind, muss der Adressbuchhierarchie �bermittlung behandeln, festgelegt, mit den Werten der entsprechenden **PR_SENDER** Eigenschaften. Wenn die **PR_SENT_REPRESENTING** Eigenschaften verf�gbar sind, aber der Adressbuchhierarchie keine Zugriffsrechte f�r Stellvertretung unterst�tzt, k�nnen sie die **PR_SENDER** -Eigenschaften f�r die �bermittlung verwenden. 
  

