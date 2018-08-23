---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592689"
---
# <a name="iolkenum"></a><span data-ttu-id="d2a71-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d2a71-102">IOlkEnum</span></span>

<span data-ttu-id="d2a71-103">Aufzählen von Konten als [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2a71-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d2a71-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d2a71-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2a71-105">Erbt:</span><span class="sxs-lookup"><span data-stu-id="d2a71-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="d2a71-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2a71-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="d2a71-107">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d2a71-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2a71-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="d2a71-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="d2a71-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="d2a71-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="d2a71-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="d2a71-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="d2a71-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d2a71-111">Called by:</span></span>  <br/> |<span data-ttu-id="d2a71-112">Client</span><span class="sxs-lookup"><span data-stu-id="d2a71-112">Client</span></span>  <br/> |
|<span data-ttu-id="d2a71-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="d2a71-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d2a71-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d2a71-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d2a71-115">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d2a71-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d2a71-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="d2a71-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="d2a71-117">Ruft die Anzahl von Konten in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="d2a71-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d2a71-118">Reset</span><span class="sxs-lookup"><span data-stu-id="d2a71-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="d2a71-119">Setzt den Enumerator auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="d2a71-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="d2a71-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="d2a71-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="d2a71-121">Ruft das nächste Konto in den Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="d2a71-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d2a71-122">Überspringen</span><span class="sxs-lookup"><span data-stu-id="d2a71-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="d2a71-123">Überspringt eine angegebene Anzahl von Konten in den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="d2a71-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2a71-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d2a71-124">Remarks</span></span>

<span data-ttu-id="d2a71-125">Diese Schnittstelle wird von **IOlkAccountManager::EnumerateAccounts** zurückgegeben, wenn einen Enumerator von Konten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2a71-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2a71-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2a71-126">See also</span></span>

- [<span data-ttu-id="d2a71-127">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="d2a71-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d2a71-128">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="d2a71-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

