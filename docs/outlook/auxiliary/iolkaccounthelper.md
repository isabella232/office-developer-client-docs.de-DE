---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322155"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="e85d1-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e85d1-102">IOlkAccountHelper</span></span>

<span data-ttu-id="e85d1-103">Stellt Hilfsfunktionen in der aktuellen MAPI-Sitzung zum Verwalten von Konten bereit.</span><span class="sxs-lookup"><span data-stu-id="e85d1-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e85d1-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e85d1-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e85d1-105">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="e85d1-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="e85d1-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e85d1-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e85d1-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="e85d1-107">Provided by:</span></span>  <br/> |<span data-ttu-id="e85d1-108">Client</span><span class="sxs-lookup"><span data-stu-id="e85d1-108">Client</span></span>  <br/> |
|<span data-ttu-id="e85d1-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="e85d1-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e85d1-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e85d1-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e85d1-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e85d1-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e85d1-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="e85d1-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="e85d1-113">*Dieser Member ist ein Platzhalter und wird nicht unterstützt.*</span><span class="sxs-lookup"><span data-stu-id="e85d1-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="e85d1-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="e85d1-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="e85d1-115">Ruft den Profilnamen eines Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="e85d1-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="e85d1-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="e85d1-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="e85d1-117">Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Kontomanager.</span><span class="sxs-lookup"><span data-stu-id="e85d1-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="e85d1-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="e85d1-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="e85d1-119">Gibt das MAPI-Sitzungsobjekt frei, das von [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e85d1-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e85d1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e85d1-120">Remarks</span></span>

<span data-ttu-id="e85d1-121">Diese Schnittstelle wird an [IOlkAccountManager:: init](iolkaccountmanager-init.md) übergeben, wenn der Konto-Manager initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e85d1-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e85d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e85d1-122">See also</span></span>

- [<span data-ttu-id="e85d1-123">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="e85d1-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e85d1-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="e85d1-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

