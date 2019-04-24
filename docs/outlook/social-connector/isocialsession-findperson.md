---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem Parameter userID übereinstimmen.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285371"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="5c9cd-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="5c9cd-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="5c9cd-104">Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem Parameter _UserID_ übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5c9cd-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="5c9cd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c9cd-105">Parameters</span></span>

<span data-ttu-id="5c9cd-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="5c9cd-106">_userId_</span></span>
  
> <span data-ttu-id="5c9cd-107">in Eine soziale Netzwerk-Benutzer-ID, SMTP-Adresse oder Anzeigename einer Person.</span><span class="sxs-lookup"><span data-stu-id="5c9cd-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="5c9cd-108">_result_</span><span class="sxs-lookup"><span data-stu-id="5c9cd-108">_result_</span></span>
  
> <span data-ttu-id="5c9cd-109">Out Eine XML-Zeichenfolge, die eine oder mehrere Personen darstellt, die mit den vom _UserID_ -Parameter angegebenen Identifikationsinformationen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5c9cd-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c9cd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c9cd-110">Remarks</span></span>

<span data-ttu-id="5c9cd-111">Wenn eine oder mehrere Personen mit der **FindPerson** -Anforderung übereinstimmen, gibt diese Methode die Informationen für diese Personen im _Result_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="5c9cd-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="5c9cd-112">Die XML- _Ergebnis_ Zeichenfolge muss mit der Schema Definition für **Freunde**übereinstimmen, wie im Schema für die Erweiterbarkeit des osc-Anbieters für Outlook (Social Connector) definiert.</span><span class="sxs-lookup"><span data-stu-id="5c9cd-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c9cd-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c9cd-113">See also</span></span>

- [<span data-ttu-id="5c9cd-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c9cd-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

