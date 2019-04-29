---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Ruft eine Zeichenfolge ab, die Details für die Person darstellt, wie den Vornamen, den Nachnamen und eine URL zu einem Profilbild.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427332"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="92cc4-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="92cc4-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="92cc4-104">Ruft eine Zeichenfolge ab, die Details für die Person darstellt, wie den Vornamen, den Nachnamen und eine URL zu einem Profilbild.</span><span class="sxs-lookup"><span data-stu-id="92cc4-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="92cc4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="92cc4-105">Parameters</span></span>

<span data-ttu-id="92cc4-106">_details_</span><span class="sxs-lookup"><span data-stu-id="92cc4-106">_details_</span></span>
  
> <span data-ttu-id="92cc4-107">Out Ein XML-Zeichenfolgenwert, der die Details für eine Person darstellt.</span><span class="sxs-lookup"><span data-stu-id="92cc4-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92cc4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92cc4-108">Remarks</span></span>

<span data-ttu-id="92cc4-109">Die XML-Zeichenfolge zurückgegebene _Details_ muss mit der Schema Definition für **Person**übereinstimmen, wie im Schema for Outlook Social Connector (OSC)-Anbieter Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="92cc4-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="92cc4-110">OSC ruft **getDetails** auf, wenn der osc-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92cc4-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="92cc4-111">Wenn der OSC anfänglich die Aktivitäten von Freunden für den angemeldeten Benutzer abruft, ruft er [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)auf und speichert die Informationen der Freunde in einem für das soziale netzwerkspezifischen Kontakteordner im standardmäßigen Outlook-Speicher des angemeldeten Benutzers. .</span><span class="sxs-lookup"><span data-stu-id="92cc4-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="92cc4-112">Anschließend ruft der OSC **GetFriendsAndColleagues** oder getDetails \*\*\*\* nur auf, wenn das Aktualisierungsintervall für den Cache abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="92cc4-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="92cc4-113">Weitere Informationen dazu, wie der OSC Freundes Informationen in einem Ordner Kontakte speichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="92cc4-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92cc4-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92cc4-114">See also</span></span>

- [<span data-ttu-id="92cc4-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92cc4-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

