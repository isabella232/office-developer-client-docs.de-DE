---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert einen Benutzer, der Frei/Gebucht-Daten möglicherweise nicht zur Verfügung hat.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317661"
---
# <a name="fbuser"></a><span data-ttu-id="be6f2-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="be6f2-103">FBUser</span></span>

<span data-ttu-id="be6f2-104">Identifiziert einen Benutzer, der Frei/Gebucht-Daten möglicherweise nicht zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="be6f2-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="be6f2-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="be6f2-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="be6f2-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="be6f2-106">Members</span></span>

<span data-ttu-id="be6f2-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="be6f2-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="be6f2-108">Die Länge der Eintrags-ID des e-Mail-Benutzers, der von der [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="be6f2-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="be6f2-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="be6f2-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="be6f2-110">Die Eintrags-ID des e-Mail-Benutzers, der von der **IMailUser** -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="be6f2-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="be6f2-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="be6f2-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="be6f2-112">Dieser Parameter ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be6f2-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="be6f2-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="be6f2-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="be6f2-114">Dieser Parameter ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be6f2-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be6f2-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be6f2-115">See also</span></span>

- [<span data-ttu-id="be6f2-116">Über die Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="be6f2-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="be6f2-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="be6f2-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

