---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialisiert den Outlook Social Connector (OSC)-Anbieter.
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285759"
---
# <a name="isocialproviderload"></a><span data-ttu-id="e3044-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="e3044-103">ISocialProvider::Load</span></span>

<span data-ttu-id="e3044-104">Initialisiert den Outlook Social Connector (OSC)-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="e3044-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="e3044-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3044-105">Parameters</span></span>

<span data-ttu-id="e3044-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="e3044-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="e3044-107">in Die Version der OSC-Anbieterschnittstellen, die vom OSC erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="e3044-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="e3044-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="e3044-108">_languageTag_</span></span>
  
> <span data-ttu-id="e3044-109">in Das von [[rfc4646]](https://www.ietf.org/rfc/rfc4646.txt) und [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)definierte IETF-Sprachtag (Internet Engineering Task Force), das die aktuelle Sprache der Benutzeroberfläche von Outlook darstellt.</span><span class="sxs-lookup"><span data-stu-id="e3044-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3044-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3044-110">Remarks</span></span>

<span data-ttu-id="e3044-111">Das Versionsformat für den _socialProviderInterfaceVersion_ -Parameter ist _X_. _xxxx_, wobei _X_ die Hauptversion ist und _xxxx_ die Nebenversion des osc ist.</span><span class="sxs-lookup"><span data-stu-id="e3044-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="e3044-112">Für Office 2013 überprüfen Sie, ob die Hauptversion 15 ist.</span><span class="sxs-lookup"><span data-stu-id="e3044-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3044-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3044-113">See also</span></span>

- [<span data-ttu-id="e3044-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3044-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

