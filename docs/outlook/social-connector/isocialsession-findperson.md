---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem parameter userID übereinstimmen.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434795"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="04388-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="04388-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="04388-104">Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem _parameter userID übereinstimmen._</span><span class="sxs-lookup"><span data-stu-id="04388-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="04388-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="04388-105">Parameters</span></span>

<span data-ttu-id="04388-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="04388-106">_userId_</span></span>
  
> <span data-ttu-id="04388-107">[in] Eine Benutzer-ID des sozialen Netzwerks, eine SMTP-Adresse oder ein Anzeigename einer Person.</span><span class="sxs-lookup"><span data-stu-id="04388-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="04388-108">_result_</span><span class="sxs-lookup"><span data-stu-id="04388-108">_result_</span></span>
  
> <span data-ttu-id="04388-109">[out] Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die den vom parameter userId angegebenen  _Identifikationsinformationen_ entsprechen.</span><span class="sxs-lookup"><span data-stu-id="04388-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="04388-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04388-110">Remarks</span></span>

<span data-ttu-id="04388-111">Wenn eine oder mehrere Personen mit der **FindPerson-Anforderung** übereinstimmen, gibt diese Methode die Informationen für diese Personen im  _Ergebnisparameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="04388-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="04388-112">Die  Ergebnis-XML-Zeichenfolge muss der Schemadefinition für Freunde **entsprechen,** wie sie im Schema für die Erweiterbarkeit des Outlook Social Connector (OSC) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="04388-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04388-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04388-113">See also</span></span>

- [<span data-ttu-id="04388-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04388-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

