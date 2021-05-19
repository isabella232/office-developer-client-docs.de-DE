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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425393"
---
# <a name="copying-a-message-service"></a>Kopieren eines Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So kopieren Sie einen Nachrichtendienst in ein Profil**
  
- Rufen [Sie IMsgServiceAdmin::CopyMsgService auf.](imsgserviceadmin-copymsgservice.md)
    
Wenn ein Nachrichtendienst kopiert wird, wird die neue Instanz des Diensts auf die gleiche Weise wie das Original konfiguriert. Manchmal **gibt CopyMsgService** den Fehler MAPI_E_ACCESS_DENIED. Die häufigste Ursache für diese Fehlerrückmeldung ist ein Nachrichtendienst, der sich nicht duplizieren lässt. 
  

