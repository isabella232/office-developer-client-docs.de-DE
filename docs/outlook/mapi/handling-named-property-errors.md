---
title: Behandeln von Fehlern bei benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429866"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="2f698-103">Behandeln von Fehlern bei benannten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f698-103">Handling named property errors</span></span>
  
<span data-ttu-id="2f698-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f698-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span><span class="sxs-lookup"><span data-stu-id="2f698-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="2f698-107">Wenn ein Anruf f�hrt partielle Erfolg, beispielsweise wenn die Anforderung f�r die Namen von ist, die bestimmte Bezeichner zuordnen und einen oder mehrere Namen gefunden werden k�nnen, **GetNamesFromIDs** MAPI_W_ERRORS_RETURNED zur�ckgibt und platziert PT_ERROR in den Eigenschaftstyp f�r die fehlenden Eigenschaft im Array Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2f698-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="2f698-p102">In einigen F�llen ein Client sendet einen Anruf an **GetNamesFromIDs**, der keine Eigenschaften zur�ckgegeben werden, z. B., wenn es sind keine Eigenschaften in einem angegebenen Eigenschaftensatz oder alle benannte Eigenschaften eines Typs werden durch die Kennzeichen ausgeschlossen werden. Clients k�nnen Dienstanbieter zu erwarten:</span><span class="sxs-lookup"><span data-stu-id="2f698-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="2f698-110">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="2f698-110">Return S_OK.</span></span>
    
- <span data-ttu-id="2f698-111">Legen Sie den Inhalt der Eigenschaft Tag Array Zeiger in ein Array der neu zugeordnete Eigenschaft Tag mit seinem **cValues** Mitglied auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f698-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="2f698-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span><span class="sxs-lookup"><span data-stu-id="2f698-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="2f698-113">Legen Sie den Inhalt der Anzahl **MAPINAMEID** Strukturen auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2f698-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2f698-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f698-114">See also</span></span>

- [<span data-ttu-id="2f698-115">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="2f698-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

