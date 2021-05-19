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
  
Viele Transportanbieter senden automatisch alle ausgehenden Nachrichten mit dem Transport Neutral Encapsulation Format (TNEF). TNEF wird verwendet, um den formatierten Text zu übertragen, den viele Clients und Nachrichtenspeicheranbieter in ihren Nachrichten, Anlagen verschiedener Typen und benutzerdefinierte Eigenschaften für benutzerdefinierte Nachrichtenklassen unterstützen. Obwohl der Standardmodus für die meisten Transportanbieter das Senden ausgehender Nachrichten mit TNEF ist, werden diese von einigen Transportanbietern nicht unterstützt. Die fehlende Unterstützung für TNEF ist kein Problem für Standardnachrichtenclients, die IPM-Nachrichten senden und empfangen. Für formularbasierte Clients oder Clients, die benutzerdefinierte Eigenschaften erfordern, ist die Verwendung von TNEF jedoch unerlässlich. Designer von Clients, die auf Formularen oder benutzerdefinierten Eigenschaften beruhen, müssen sich der Funktionen der von ihnen verwendeten Transportanbieter bewusst sein.
  
Nachrichtenempfänger können steuern, ob ein Transportanbieter Nachrichten mit TNEF überträgt, indem sie die **PR_SEND_RICH_INFO** festlegen. Weitere Informationen finden Sie unter **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Wenn die Eigenschaft **PR_SEND_RICH_INFO** Empfängers auf TRUE festgelegt ist, überträgt ein Transportanbieter, der TNEF unterstützt, diese mit der Nachricht. Wenn die Eigenschaft auf FALSE festgelegt ist, wird die Formatierung verworfen. Wenn **PR_SEND_RICH_INFO** nicht vorhanden ist, ist es an dem Transportanbieter, einen Standardaktionsverlauf zu wählen. 
  
Wenn Clients und Dienstanbieter einen benutzerdefinierten Empfänger erstellen, können sie sich auf den Wert der **PR_SEND_RICH_INFO-Eigenschaft** auswirken, indem sie das MAPI_SEND_NO_RICH_INFO-Flag im  _ulFlags-Parameter_ an den **IAddrBook::CreateOneOff-** oder **IMAPISupport::CreateOneOff-Aufruf** übergeben. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Durch MAPI_SEND_NO_RICH_INFO wird die #A0 des benutzerdefinierten Empfängers **PR_SEND_RICH_INFO** FALSE festgelegt. In den meisten Fällen wird die Eigenschaft von MAPI nicht auf TRUE festgelegt. Die einzige Ausnahme ist, wenn die Adresse des benutzerdefinierten Empfängers als Internetadresse interpretiert wird. In dieser einen Situation legt MAPI **PR_SEND_RICH_INFO** FALSE fest. 
  

