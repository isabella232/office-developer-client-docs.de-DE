---
title: Unterst�tzung f�r benannte Eigenschaften im Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1aa0228cdc8cf6f0b2bb321e62e40127775a6de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795666"
---
# <a name="supporting-named-properties-in-message-stores"></a>Unterst�tzung f�r benannte Eigenschaften im Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Definieren von neuen MAPI-Eigenschaften](defining-new-mapi-properties.md) and [Unterst�tzung f�r benannte Eigenschaften](supporting-named-properties.md).
  
Die meisten Nachrichtenspeichers Anbieter, unterst�tzen, mit dem Namen Eigenschaften verwenden eine einzelne Zuordnung Signatur f�r alle Objekte in der Nachrichtenspeicher. Dies bietet zwei Vorteile. Erstens ist es einfacher, Zuordnung Signaturen implementieren, wenn es nur eine ist zu verfolgen. Zweitens Wenn alle Objekte in der Nachrichtenspeicher die gleiche Zuordnung Signatur verwenden, k�nnen Clientanwendungen sicher sein, dass alle Eigenschaftenbezeichner f�r Nachrichten im Nachrichtenspeicher tats�chlich auf dieselbe benannte Eigenschaft zu verweisen. Auf diese Weise k�nnen die Client-Anwendungen in ihrer Ordneransicht Spalten f�r benannte Eigenschaften anzuzeigen.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeicher](implementing-messages-in-message-stores.md)

