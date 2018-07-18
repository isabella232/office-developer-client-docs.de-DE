---
title: Löschen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791523"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="634ea-103">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="634ea-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="634ea-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="634ea-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="634ea-105">**So löschen Sie eine Message Service aus einem Profil**</span><span class="sxs-lookup"><span data-stu-id="634ea-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="634ea-106">Rufen Sie **IMAPISession::GetMsgServiceTable** die Tabelle der Dienste für den Zugriff auf.</span><span class="sxs-lookup"><span data-stu-id="634ea-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="634ea-107">Suchen Sie die Zeile für den Dienst, und übergeben Sie die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im Parameter _Lpuid_ an [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="634ea-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="634ea-108">**DeleteMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="634ea-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="634ea-109">Message-Dienste Ausführen von Aufgaben zu diesem Zeitpunkt aus, bevor sie aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="634ea-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

