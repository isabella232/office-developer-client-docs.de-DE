---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge, die eine oder mehrere Personen darstellt, die den Benutzer-ID-Parameter entsprechen.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795983"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="625c9-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="625c9-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="625c9-104">Ruft eine Zeichenfolge, die eine oder mehrere Personen darstellt, die den _Benutzer-ID_ -Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="625c9-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="625c9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="625c9-105">Parameters</span></span>

<span data-ttu-id="625c9-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="625c9-106">_userId_</span></span>
  
> <span data-ttu-id="625c9-107">[in] Eine Benutzer-ID für soziale Netzwerke, SMTP-Adresse oder Anzeigename den Namen einer Person.</span><span class="sxs-lookup"><span data-stu-id="625c9-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="625c9-108">_Ergebnis_</span><span class="sxs-lookup"><span data-stu-id="625c9-108">_result_</span></span>
  
> <span data-ttu-id="625c9-109">[out] Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die durch den _Benutzer-ID_ -Parameter angegebenen Informationen zur Identifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="625c9-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="625c9-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="625c9-110">Remarks</span></span>

<span data-ttu-id="625c9-111">Wenn eine oder mehrere Personen die Anforderung **FindPerson** übereinstimmen, gibt diese Methode die Informationen für die Personen in der _Result_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="625c9-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="625c9-112">Die _resultierende_ XML-Zeichenfolge muss der Schemadefinition für **Freunde**, gemäß Definition im Schema für Outlook Social Connector (OSC)-Erweiterbarkeit des Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="625c9-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="625c9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="625c9-113">See also</span></span>

- [<span data-ttu-id="625c9-114">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="625c9-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

