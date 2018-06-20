---
title: Kopieren eines Nachricht-Diensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791431"
---
# <a name="copying-a-message-service"></a>Kopieren eines Nachricht-Diensts

  
  
**Betrifft**: Outlook 
  
 **Kopieren einer Messagingdiensts zu einem Profil**
  
- Rufen Sie [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Wenn ein Nachrichtendienst kopiert wird, ist die neue Instanz des Diensts auf genau die gleiche Weise wie die ursprüngliche konfiguriert. In einigen Fällen wird **CopyMsgService** der Fehler MAPI_E_ACCESS_DENIED zurückgegeben. Die häufigste Ursache für diese Fehler Return ist ein Nachrichtendienst, der nicht selbst zu duplizierende zulässt. 
  

