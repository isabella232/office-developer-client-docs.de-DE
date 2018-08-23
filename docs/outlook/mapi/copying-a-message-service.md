---
title: Kopieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573719"
---
# <a name="copying-a-message-service"></a>Kopieren eines Nachrichtendiensts

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **Kopieren einer Messagingdiensts zu einem Profil**
  
- Rufen Sie [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Wenn ein Nachrichtendienst kopiert wird, ist die neue Instanz des Diensts auf genau die gleiche Weise wie die ursprüngliche konfiguriert. In einigen Fällen wird **CopyMsgService** der Fehler MAPI_E_ACCESS_DENIED zurückgegeben. Die häufigste Ursache für diese Fehler Return ist ein Nachrichtendienst, der nicht selbst zu duplizierende zulässt. 
  

