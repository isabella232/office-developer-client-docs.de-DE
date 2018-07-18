---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790930"
---
# <a name="fbuser"></a><span data-ttu-id="bf082-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="bf082-103">FBUser</span></span>

<span data-ttu-id="bf082-104">Identifiziert ein Benutzer, der möglicherweise keinen Daten Frei/Gebucht-Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf082-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bf082-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="bf082-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="bf082-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="bf082-106">Members</span></span>

<span data-ttu-id="bf082-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="bf082-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="bf082-108">Die Länge des Eintrags-ID des e-Mail-Benutzers dargestellt durch die [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf082-108">The length of the entry ID of the mail user as represented by the [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) interface.</span></span> 
    
<span data-ttu-id="bf082-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="bf082-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="bf082-110">Die Eintrags-ID des e-Mail-Benutzers dargestellt durch die **IMailUser** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf082-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="bf082-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="bf082-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="bf082-112">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf082-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="bf082-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="bf082-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="bf082-114">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf082-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf082-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf082-115">See also</span></span>

- [<span data-ttu-id="bf082-116">Über die Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="bf082-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="bf082-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="bf082-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

