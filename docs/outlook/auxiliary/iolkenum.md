---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322099"
---
# <a name="iolkenum"></a><span data-ttu-id="98197-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="98197-102">IOlkEnum</span></span>

<span data-ttu-id="98197-103">Unterstützt das Aufzählen von Konten als [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="98197-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="98197-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="98197-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98197-105">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="98197-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="98197-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="98197-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="98197-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="98197-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="98197-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="98197-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="98197-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="98197-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="98197-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="98197-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="98197-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="98197-111">Called by:</span></span>  <br/> |<span data-ttu-id="98197-112">Client</span><span class="sxs-lookup"><span data-stu-id="98197-112">Client</span></span>  <br/> |
|<span data-ttu-id="98197-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="98197-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="98197-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="98197-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="98197-115">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="98197-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="98197-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="98197-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="98197-117">Ruft die Anzahl der Konten im Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="98197-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="98197-118">Reset</span><span class="sxs-lookup"><span data-stu-id="98197-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="98197-119">Setzt den Enumerator auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="98197-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="98197-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="98197-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="98197-121">Ruft das nächste Konto im Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="98197-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="98197-122">Skip</span><span class="sxs-lookup"><span data-stu-id="98197-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="98197-123">Überspringt eine angegebene Anzahl von Konten im Enumerator.</span><span class="sxs-lookup"><span data-stu-id="98197-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98197-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98197-124">Remarks</span></span>

<span data-ttu-id="98197-125">Diese Schnittstelle wird von **IOlkAccountManager:: EnumerateAccounts** zurückgegeben, wenn ein Enumerator von Konten abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="98197-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98197-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98197-126">See also</span></span>

- [<span data-ttu-id="98197-127">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="98197-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="98197-128">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="98197-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

