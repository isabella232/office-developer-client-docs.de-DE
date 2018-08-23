---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565137"
---
# <a name="fbuser"></a><span data-ttu-id="46c27-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="46c27-103">FBUser</span></span>

<span data-ttu-id="46c27-104">Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46c27-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46c27-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="46c27-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="46c27-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="46c27-106">Members</span></span>

<span data-ttu-id="46c27-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="46c27-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="46c27-108">Die Länge des Eintrags-ID des e-Mail-Benutzers dargestellt durch die [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="46c27-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="46c27-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="46c27-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="46c27-110">Die Eintrags-ID des e-Mail-Benutzers dargestellt durch die **IMailUser** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="46c27-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="46c27-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="46c27-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="46c27-112">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46c27-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="46c27-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="46c27-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="46c27-114">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46c27-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46c27-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c27-115">See also</span></span>

- [<span data-ttu-id="46c27-116">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="46c27-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="46c27-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="46c27-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

