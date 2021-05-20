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
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428123"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="0eb94-103">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="0eb94-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="0eb94-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eb94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0eb94-105">**So löschen Sie einen Nachrichtendienst aus einem Profil**</span><span class="sxs-lookup"><span data-stu-id="0eb94-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="0eb94-106">Rufen **Sie IMAPISession::GetMsgServiceTable auf,** um auf die Nachrichtendiensttabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0eb94-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="0eb94-107">Suchen Sie die Zeile für den **Nachrichtendienst, und** übergeben Sie die spalte PR_SERVICE_UID ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) im  _lpuid-Parameter_ an [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="0eb94-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="0eb94-108">**DeleteMsgService** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, der  _ulContext-Parameter_ ist auf MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="0eb94-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="0eb94-109">Nachrichtendienste führen zu diesem Zeitpunkt alle Bereinigungsaufgaben aus, bevor sie aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0eb94-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

