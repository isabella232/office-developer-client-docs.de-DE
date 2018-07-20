---
title: Umgang mit der Eigenschaftenfehler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ea1c4063c08844052618c50fe53fdc0064787a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791808"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="edd11-103">Umgang mit der Eigenschaftenfehler</span><span class="sxs-lookup"><span data-stu-id="edd11-103">Handling named property errors</span></span>
  
<span data-ttu-id="edd11-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edd11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edd11-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span><span class="sxs-lookup"><span data-stu-id="edd11-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="edd11-107">Wenn ein Anruf führt partielle Erfolg, beispielsweise wenn die Anforderung für die Namen von ist, die bestimmte Bezeichner zuordnen und einen oder mehrere Namen gefunden werden können, **GetNamesFromIDs** MAPI_W_ERRORS_RETURNED zurückgibt und platziert PT_ERROR in den Eigenschaftstyp für die fehlenden Eigenschaft im Array Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="edd11-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="edd11-p102">In einigen Fällen ein Client sendet einen Anruf an **GetNamesFromIDs**, der keine Eigenschaften zurückgegeben werden, z. B., wenn es sind keine Eigenschaften in einem angegebenen Eigenschaftensatz oder alle benannte Eigenschaften eines Typs werden durch die Kennzeichen ausgeschlossen werden. Clients können Dienstanbieter zu erwarten:</span><span class="sxs-lookup"><span data-stu-id="edd11-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="edd11-110">Geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="edd11-110">Return S_OK.</span></span>
    
- <span data-ttu-id="edd11-111">Legen Sie den Inhalt der Eigenschaft Tag Array Zeiger in ein Array der neu zugeordnete Eigenschaft Tag mit seinem **cValues** Mitglied auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="edd11-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="edd11-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span><span class="sxs-lookup"><span data-stu-id="edd11-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="edd11-113">Legen Sie den Inhalt der Anzahl **MAPINAMEID** Strukturen auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="edd11-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="edd11-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd11-114">See also</span></span>

- [<span data-ttu-id="edd11-115">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="edd11-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

