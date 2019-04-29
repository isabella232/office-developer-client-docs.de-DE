---
title: Senden von Nachrichten mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7ff7f79b5e74412e9bbb4b4882c6a7d45e50fe6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420850"
---
# <a name="sending-messages-with-tnef"></a>Senden von Nachrichten mit TNEF

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Transportanbieter senden automatisch alle ausgehenden Nachrichten mit dem Transport Neutral Encapsulation Format (TNEF). TNEF wird verwendet, um den formatierten Text zu übertragen, den viele Clients und Nachrichtenspeicher Anbieter in ihren Nachrichten, Anlagen verschiedener Typen und benutzerdefinierten Eigenschaften für benutzerdefinierte Nachrichtenklassen unterstützen. Obwohl der Standardmodus für die meisten Transportanbieter das Senden ausgehender Nachrichten mit TNEF ist, werden diese von einigen Transportanbietern nicht unterstützt. Die mangelnde Unterstützung für TNEF ist kein Problem für standardmäßige Messagingclients, die IPM-Nachrichten senden und empfangen. Für formularbasierte Clients oder Clients, die benutzerdefinierte Eigenschaften erfordern, ist jedoch die Verwendung von TNEF unerlässlich. Designer von Clients, die auf Formularen oder benutzerdefinierten Eigenschaften basieren, müssen die Funktionen der verwendeten Transportanbieter kennen.
  
Nachrichtenempfänger können steuern, ob ein Transportanbieter Nachrichten mit TNEF übermittelt, indem Sie die **PR_SEND_RICH_INFO** -Eigenschaft festlegen. Weitere Informationen finden Sie unter **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md)). Wenn die **PR_SEND_RICH_INFO** -Eigenschaft eines Empfängers auf true festgelegt ist, übermittelt ein Transportanbieter, der TNEF unterstützt, ihn mit der Nachricht. Wenn die Eigenschaft auf FALSE festgelegt ist, wird die Formatierung verworfen. Wenn **PR_SEND_RICH_INFO** nicht vorhanden ist, muss der Transportanbieter eine Standardaktion auswählen. 
  
Wenn Clients und Dienstanbieter einen benutzerdefinierten Empfänger erstellen, können Sie sich auf den Wert der **PR_SEND_RICH_INFO** -Eigenschaft auswirken, indem Sie das MAPI_SEND_NO_RICH_INFO-Flag im _ulFlags_ -Parameter an die **IAddrBook:: CreateOneOff** oder ** IMAPISupport:: CreateOneOff** -Aufruf. Weitere Informationen finden Sie unter [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Durch das Übergeben von MAPI_SEND_NO_RICH_INFO wird von MAPI die **PR_SEND_RICH_INFO** -Eigenschaft des benutzerdefinierten Empfängers auf false festgelegt. in den meisten Fällen, die das Flag nicht übergeben, bewirkt MAPI, dass die Eigenschaft auf TRUE festgelegt wird. Die einzige Ausnahme ist, wenn die Adresse des benutzerdefinierten Empfängers als Internet Adresse interpretiert wird. In dieser Situation wird **PR_SEND_RICH_INFO** auf "false" festgelegt. 
  

