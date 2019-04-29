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
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439863"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Unterst�tzung von mehreren den Clientzugriff auf Nachrichten in Nachrichtenspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es ist m�glich, dass mehrere Clientanwendungen, eine bestimmte Nachricht gleichzeitig zu �ffnen. Nachricht-Anbieter m�ssen keine f�hren bestimmten Regeln f�r diesen Zugriff steuern. Wenn die Client-Anwendungen �ndern Sie die Nachricht und ihre �nderungen zu speichern, sollten jedoch Speicheranbieter die folgenden Regeln entsprechen:
  
- Zulassen der erste Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um fortzufahren, als w�re es der einzige Client, der die Nachricht ge�ffnet hat. 
    
- Die nachfolgenden **SaveChanges** Anrufe von anderen Clients sollte der Nachricht Speicheranbieter �nderungen ignorieren und MAPI_E_OBJECT_CHANGED zur�ck. 
    
- Erm�glichen Sie Clientanwendungen Reaktion auf einen MAPI_E_OBJECT_CHANGED R�ckgabecode durch den aufrufenden **SaveChanges** erneut mit dem FORCE_SAVE-Flag. Wenn eine Clientanwendung dies der Fall ist, sollten vom Informationsdienst Nachricht die vorherigen �nderungen mit den neuen zu ersetzen. 
    
Alternativ kann die Nachrichtenanbieter den Konflikt zu erkennen und pr�sentieren eine Schnittstelle, die erm�glicht dem Benutzer das ausw�hlen, ob die urspr�ngliche Nachricht beibehalten, die urspr�ngliche Nachricht mit den neuen �nderungen �berschreiben oder speichern Sie die neuen �nderungen an einen anderen Speicherort.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeichern](implementing-messages-in-message-stores.md)

