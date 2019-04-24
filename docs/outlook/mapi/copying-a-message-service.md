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
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333054"
---
# <a name="copying-a-message-service"></a>Kopieren eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So kopieren Sie einen Nachrichtendienst in ein Profil**
  
- Rufen Sie [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md)auf.
    
Wenn ein Nachrichtendienst kopiert wird, wird die neue Instanz des Diensts genau auf die gleiche Weise konfiguriert wie das Original. Manchmal gibt **CopyMsgService** den Fehler MAPI_E_ACCESS_DENIED zurück. Die häufigste Ursache für diesen Fehler ist ein Nachrichtendienst, der nicht dupliziert werden kann. 
  

