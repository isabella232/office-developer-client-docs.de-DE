---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Bestimmt, ob die angegebenen Benutzer Freunde sind.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331668"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="59862-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="59862-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="59862-104">Bestimmt, ob die angegebenen Benutzer Freunde sind.</span><span class="sxs-lookup"><span data-stu-id="59862-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="59862-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="59862-105">Parameters</span></span>

<span data-ttu-id="59862-106">_UserIds_</span><span class="sxs-lookup"><span data-stu-id="59862-106">_userIds_</span></span>
  
> <span data-ttu-id="59862-107">in Eine Struktur, die ein Array von Benutzer-ID-Werten angibt, die einer Gruppe von Personen im sozialen Netzwerk entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59862-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="59862-108">_Ergebnisse_</span><span class="sxs-lookup"><span data-stu-id="59862-108">_results_</span></span>
  
> <span data-ttu-id="59862-109">Out Ein Zeiger auf Structure, der ein Array von booleschen Werten angibt, das angibt, ob die entsprechende __ Person im userids-Array ein Freund ist.</span><span class="sxs-lookup"><span data-stu-id="59862-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59862-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59862-110">Remarks</span></span>

<span data-ttu-id="59862-111">Für jede im Eingabearray des userids-para __ meters dargestellte Person legt diese Methode das entsprechende Element im Ausgabearray des Parameters _results_ fest.</span><span class="sxs-lookup"><span data-stu-id="59862-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="59862-112">**true** gibt an, dass die Person ein Freund ist, und **false** gibt an, dass die Person kein Freund ist.</span><span class="sxs-lookup"><span data-stu-id="59862-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59862-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59862-113">See also</span></span>

- [<span data-ttu-id="59862-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="59862-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

