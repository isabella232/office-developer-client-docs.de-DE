---
title: Löschen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583568"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="b6b5a-103">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="b6b5a-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="b6b5a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b6b5a-105">**So löschen Sie eine Message Service aus einem Profil**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="b6b5a-106">Rufen Sie **IMAPISession::GetMsgServiceTable** die Tabelle der Dienste für den Zugriff auf.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="b6b5a-107">Suchen Sie die Zeile für den Dienst, und übergeben Sie die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im Parameter _Lpuid_ an [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="b6b5a-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="b6b5a-108">**DeleteMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="b6b5a-109">Message-Dienste Ausführen von Aufgaben zu diesem Zeitpunkt aus, bevor sie aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

