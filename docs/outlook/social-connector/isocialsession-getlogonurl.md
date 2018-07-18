---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Ruft eine Zeichenfolge, die eine URL darstellt, die für die Darstellung eines Formulars browserbasierte für dem Benutzer während der Webauthentifizierung verwendet wird.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795982"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="789f4-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="789f4-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="789f4-104">Ruft eine Zeichenfolge, die eine URL darstellt, die für die Darstellung eines Formulars browserbasierte für dem Benutzer während der Webauthentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="789f4-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="789f4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="789f4-105">Parameters</span></span>

<span data-ttu-id="789f4-106">_url_</span><span class="sxs-lookup"><span data-stu-id="789f4-106">_url_</span></span>
  
> <span data-ttu-id="789f4-107">[out] Eine Zeichenfolge, die eine URL für das Formular in der Webauthentifizierung enthält.</span><span class="sxs-lookup"><span data-stu-id="789f4-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="789f4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="789f4-108">Remarks</span></span>

<span data-ttu-id="789f4-109">Nachdem das Formular für den Benutzer angezeigt wird, wird die [ISocialSession::LogonWeb](isocialsession-logonweb.md) -Methode mit einer leeren Zeichenfolge für den Parameter _ConnectIn_ aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="789f4-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="789f4-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="789f4-110">See also</span></span>

- [<span data-ttu-id="789f4-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="789f4-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

