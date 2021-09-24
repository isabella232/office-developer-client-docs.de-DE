---
title: Senden von Nachrichten mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 75f7ca1ef084b16c18306ba71c427e57870ae63c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550022"
---
# <a name="sending-messages-with-tnef"></a>Senden von Nachrichten mit TNEF

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Transportanbieter senden automatisch alle ausgehenden Nachrichten mit dem Transport Neutral Encapsulation Format (TNEF). TNEF wird verwendet, um den formatierten Text zu übertragen, den viele Clients und Nachrichtenspeicheranbieter in ihren Nachrichten, Anlagen verschiedener Typen und benutzerdefinierten Eigenschaften für benutzerdefinierte Nachrichtenklassen unterstützen. Obwohl der Standardmodus für die meisten Transportanbieter darin besteht, ausgehende Nachrichten mit TNEF zu senden, wird dies von einigen Transportanbietern nicht unterstützt. Die fehlende Unterstützung für TNEF ist kein Problem für Standardnachrichtenclients, die IPM-Nachrichten senden und empfangen. Für formularbasierte Clients oder Clients, die benutzerdefinierte Eigenschaften erfordern, ist jedoch die Verwendung von TNEF unerlässlich. Entwickler von Clients, die auf Formularen oder benutzerdefinierten Eigenschaften basieren, müssen die Funktionen der verwendeten Transportanbieter kennen.
  
Nachrichtenempfänger können steuern, ob ein Transportanbieter Nachrichten mit TNEF überträgt, indem sie die **eigenschaft PR_SEND_RICH_INFO** festlegen. Weitere Informationen finden Sie unter **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Wenn die **PR_SEND_RICH_INFO** Eigenschaft eines Empfängers auf TRUE festgelegt ist, überträgt ein Transportanbieter, der TNEF unterstützt, diese mit der Nachricht. Wenn die Eigenschaft auf FALSE festgelegt ist, wird die Formatierung verworfen. Wenn **PR_SEND_RICH_INFO** nicht vorhanden ist, kann der Transportanbieter eine Standardaktion auswählen. 
  
Wenn Clients und Dienstanbieter einen benutzerdefinierten Empfänger erstellen, können sie sich auf den Wert der **PR_SEND_RICH_INFO** Eigenschaft auswirken, indem sie das flag MAPI_SEND_NO_RICH_INFO im  _ulFlags-Parameter_ an den **IAddrBook::CreateOneOff-** oder **IMAPISupport::CreateOneOff-Aufruf** übergeben. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Das Übergeben MAPI_SEND_NO_RICH_INFO bewirkt, dass die MAPI die PR_SEND_RICH_INFO Eigenschaft des **benutzerdefinierten** Empfängers auf FALSE festlegt. In den meisten Fällen bewirkt das Nichtübergabe des Flags, dass MAPI die Eigenschaft auf TRUE festgelegt. Die einzige Ausnahme ist, wenn die Adresse des benutzerdefinierten Empfängers als Internetadresse interpretiert wird. In diesem Fall legt mapi **PR_SEND_RICH_INFO** auf FALSE fest. 
  

