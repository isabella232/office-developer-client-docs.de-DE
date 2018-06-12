---
title: Unterst�tzung von mehreren den Clientzugriff auf Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f48fa1712b6e09e5a73f331228a811b4eb8d284d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795660"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Unterst�tzung von mehreren den Clientzugriff auf Nachrichten in Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Es ist m�glich, dass mehrere Clientanwendungen, eine bestimmte Nachricht gleichzeitig zu �ffnen. Nachricht-Anbieter m�ssen keine f�hren bestimmten Regeln f�r diesen Zugriff steuern. Wenn die Client-Anwendungen �ndern Sie die Nachricht und ihre �nderungen zu speichern, sollten jedoch Speicheranbieter die folgenden Regeln entsprechen:
  
- Zulassen der erste Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um fortzufahren, als w�re es der einzige Client, der die Nachricht ge�ffnet hat. 
    
- Die nachfolgenden **SaveChanges** Anrufe von anderen Clients sollte der Nachricht Speicheranbieter �nderungen ignorieren und MAPI_E_OBJECT_CHANGED zur�ck. 
    
- Erm�glichen Sie Clientanwendungen Reaktion auf einen MAPI_E_OBJECT_CHANGED R�ckgabecode durch den aufrufenden **SaveChanges** erneut mit dem FORCE_SAVE-Flag. Wenn eine Clientanwendung dies der Fall ist, sollten vom Informationsdienst Nachricht die vorherigen �nderungen mit den neuen zu ersetzen. 
    
Alternativ kann die Nachrichtenanbieter den Konflikt zu erkennen und pr�sentieren eine Schnittstelle, die erm�glicht dem Benutzer das ausw�hlen, ob die urspr�ngliche Nachricht beibehalten, die urspr�ngliche Nachricht mit den neuen �nderungen �berschreiben oder speichern Sie die neuen �nderungen an einen anderen Speicherort.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeicher](implementing-messages-in-message-stores.md)

