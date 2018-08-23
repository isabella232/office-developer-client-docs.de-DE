---
title: Vermeiden bestimmter Methoden beim Start
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580635"
---
# <a name="avoiding-certain-methods-at-startup"></a>Vermeiden bestimmter Methoden beim Start

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zum Verbessern der Leistung beim Starten von vermeiden Sie die folgenden Anrufe:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Der Aufruf von **IMAPIStatus::ValidateState** wirkt sich auf die Leistung nur, wenn für die MAPI-Warteschlange oder des MAPI-Subsystems vorgenommen. Der Grund dafür, dass diese Methoden zum Starten des Verarbeitung verlangsamen besteht, da sie nicht erfüllen können, bis die MAPI-Warteschlange ihrer Aufgaben zum Starten des beendet wurde. 
  
Zudem sollten Sie Suchen des Nachrichtenspeichers beim Starten. Stellen Sie den Anruf [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) beim Start Verarbeitung beendet wurde. 
  

