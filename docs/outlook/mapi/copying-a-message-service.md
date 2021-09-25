---
title: Kopieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f3f3d505d720fb00fabcad40761e573ecd47a45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617069"
---
# <a name="copying-a-message-service"></a>Kopieren eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So kopieren Sie einen Nachrichtendienst in ein Profil**
  
- Rufen [Sie IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md)auf.
    
Wenn ein Nachrichtendienst kopiert wird, wird die neue Instanz des Diensts auf die gleiche Weise wie das Original konfiguriert. Manchmal gibt **CopyMsgService** den Fehler MAPI_E_ACCESS_DENIED zurück. Die häufigste Ursache für diese Fehlerrückgabe ist ein Nachrichtendienst, der sich nicht duplizieren lässt. 
  

