---
title: Senden von Nachrichten mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb26d854b47894d8f37763b17e5ba0b26fd25ff6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795506"
---
# <a name="sending-messages-with-tnef"></a>Senden von Nachrichten mit TNEF

  
  
**Betrifft**: Outlook 
  
Viele Transportanbieter senden automatisch alle ausgehende Nachrichten mit Transport Neutral Encapsulation Format (TNEF). TNEF wird verwendet, um der formatierte Text zu übertragen, den viele Clients und Message-Anbieter in ihre Nachrichten, die Anlagen verschiedene Arten von benutzerdefinierten Eigenschaften für benutzerdefinierte Nachrichtenklassen unterstützen. Zwar der Standardmodus für die meisten Transportanbieter zum Senden von ausgehender Nachrichten mit TNEF, Sie einige Transportanbieter nicht unterstützt. Die fehlende Unterstützung für TNEF ist kein Problem für standard messaging-Clients, die IPM Nachrichten senden und empfangen. Jedoch ist die Verwendung von TNEF für formularbasierte oder Clients, die benutzerdefinierte Eigenschaften erfordern, entscheidend. Designer von Clients, die auf Formularen oder benutzerdefinierte Eigenschaften basieren müssen die Funktionen der Transportanbieter beachten, die sie verwenden.
  
Empfänger der Nachricht können steuern, ob ein Transportdienstes Nachrichten mit TNEF durch Festlegen der Eigenschaft **PR_SEND_RICH_INFO** überträgt. Weitere Informationen finden Sie unter **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Wenn eines Empfängers **PR_SEND_RICH_INFO** -Eigenschaft auf TRUE festgelegt ist, überträgt ein Transportdienstes, das TNEF unterstützt es mit der Nachricht. Wenn die Eigenschaft auf FALSE festgelegt ist, wird die Formatierung verworfen. Wenn **PR_SEND_RICH_INFO** nicht vorhanden ist, ist es bis zu der Adressbuchhierarchie eine standardmäßige Vorgehensweise auswählen. 
  
Wenn Clients und Dienstanbieter einen benutzerdefinierten Empfänger erstellen, können diese den Wert der Eigenschaft **PR_SEND_RICH_INFO** beeinflussen, indem Sie die Kennzeichen MAPI_SEND_NO_RICH_INFO zur **IAddrBook::CreateOneOff** oder **im _UlFlags_ -Parameter übergeben IMAPISupport::CreateOneOff** aufrufen. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Übergeben von MAPI_SEND_NO_RICH_INFO bewirkt, dass MAPI, um den benutzerdefinierten Empfänger **PR_SEND_RICH_INFO** -Eigenschaft auf FALSE festgelegt. in den meisten Fällen wird durch das übergeben nicht das Flag MAPI, um die Eigenschaft auf TRUE festgelegt. Die einzige Ausnahme ist, wenn der benutzerdefinierten Empfängeradresse interpretiert wird, eine IP-Adresse sein. In diesem Fall eine wird MAPI **PR_SEND_RICH_INFO** auf false festgelegt. 
  

