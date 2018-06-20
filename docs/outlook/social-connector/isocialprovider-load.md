---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialisiert den Anbieter Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795977"
---
# <a name="isocialproviderload"></a><span data-ttu-id="a40f1-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="a40f1-103">ISocialProvider::Load</span></span>

<span data-ttu-id="a40f1-104">Initialisiert den Anbieter Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="a40f1-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="a40f1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a40f1-105">Parameters</span></span>

<span data-ttu-id="a40f1-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="a40f1-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="a40f1-107">[in] Die Version des von der OSC erwartet OSC-Provider-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a40f1-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="a40f1-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="a40f1-108">_languageTag_</span></span>
  
> <span data-ttu-id="a40f1-109">[in] Der Internet Engineering Task Force (IETF) Sprach-Tag, definiert durch [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), die die Sprache der Benutzeroberfläche von Outlook darstellt.</span><span class="sxs-lookup"><span data-stu-id="a40f1-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a40f1-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a40f1-110">Remarks</span></span>

<span data-ttu-id="a40f1-111">Das Versionsformat für den Parameter _SocialProviderInterfaceVersion_ ist _X_. _Xxxx_, wobei _X_ der Hauptversion und _Xxxx_ ist die Nebenversion der die OSC.</span><span class="sxs-lookup"><span data-stu-id="a40f1-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="a40f1-112">Überprüfen Sie für Office 2013 für die Hauptversion wird 15.</span><span class="sxs-lookup"><span data-stu-id="a40f1-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a40f1-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a40f1-113">See also</span></span>

- [<span data-ttu-id="a40f1-114">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a40f1-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

