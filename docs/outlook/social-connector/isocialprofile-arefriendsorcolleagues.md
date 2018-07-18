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
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795968"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="54857-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="54857-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="54857-104">Bestimmt, ob die angegebenen Benutzer Freunde sind.</span><span class="sxs-lookup"><span data-stu-id="54857-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="54857-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="54857-105">Parameters</span></span>

<span data-ttu-id="54857-106">_Benutzer-IDs_</span><span class="sxs-lookup"><span data-stu-id="54857-106">_userIds_</span></span>
  
> <span data-ttu-id="54857-107">[in] Eine Struktur, die ein Array von Benutzer-ID-Werte gibt an, die eine Gruppe von Personen im sozialen Netzwerk entsprechen.</span><span class="sxs-lookup"><span data-stu-id="54857-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="54857-108">_Ergebnisse_</span><span class="sxs-lookup"><span data-stu-id="54857-108">_results_</span></span>
  
> <span data-ttu-id="54857-109">[out] Ein Zeiger auf die Struktur, die ein Array von boolesche Werte zurück, der angibt, ob die entsprechende Person in das Array _Benutzer-IDs_ ein Freund ist angibt.</span><span class="sxs-lookup"><span data-stu-id="54857-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54857-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54857-110">Remarks</span></span>

<span data-ttu-id="54857-111">Für jede Person in der Eingabe der Parameter _UserIds_ gibt-Array dargestellt legt diese Methode das entsprechende Element in der Matrix des Parameters _Ergebnisse_ .</span><span class="sxs-lookup"><span data-stu-id="54857-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="54857-112">**true** gibt an, dass die Person einen Freund, und **false** gibt an, dass die Person keinen Freund ist.</span><span class="sxs-lookup"><span data-stu-id="54857-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54857-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54857-113">See also</span></span>

- [<span data-ttu-id="54857-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="54857-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

