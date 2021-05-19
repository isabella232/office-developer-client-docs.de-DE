---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419989"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="06780-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="06780-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="06780-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06780-105">Nimmt Änderungen an einem Nachrichtenspeicherprofilabschnitt dauerhaft vor.</span><span class="sxs-lookup"><span data-stu-id="06780-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="06780-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06780-106">Parameters</span></span>

 <span data-ttu-id="06780-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06780-107">_ulFlags_</span></span>
  
> <span data-ttu-id="06780-108">[in] Eine Bitmaske mit Flags, die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="06780-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="06780-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="06780-109">The following flag can be set:</span></span>
    
<span data-ttu-id="06780-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="06780-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="06780-111">Der Nachrichtenspeicher ist temporär und sollte nicht der Nachrichtenspeichertabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="06780-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="06780-112">Wenn MDB_TEMPORARY festgelegt ist, gibt **ModifyProfile** S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="06780-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="06780-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06780-113">Return value</span></span>

<span data-ttu-id="06780-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="06780-114">S_OK</span></span> 
  
> <span data-ttu-id="06780-115">Die Änderungen am Profilabschnitt waren erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="06780-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06780-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06780-116">Remarks</span></span>

<span data-ttu-id="06780-117">Die **IMAPISupport::ModifyProfile-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="06780-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="06780-118">Nachrichtenspeicheranbieter rufen **ModifyProfile auf,** um MAPI zum Ändern ihrer Profilinformationen aufforderen.</span><span class="sxs-lookup"><span data-stu-id="06780-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="06780-119">**ModifyProfile** fügt den Profilabschnitt, der dem aufrufenden Anbieter zugeordnet ist, zur Liste der installierten Ressourcen des Nachrichtenspeicheranbieters hinzu.</span><span class="sxs-lookup"><span data-stu-id="06780-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="06780-120">Dies bewirkt, dass der Nachrichtenspeicher in der Nachrichtenspeichertabelle aufgeführt wird, die Clients über die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) zur Verfügung steht, und ohne die Anzeige eines Dialogfelds geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="06780-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="06780-121">Wenn das MDB_TEMPORARY festgelegt ist, führt MAPI nichts aus, und die Methode gibt sofort mit S_OK.</span><span class="sxs-lookup"><span data-stu-id="06780-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06780-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06780-122">See also</span></span>



[<span data-ttu-id="06780-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="06780-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="06780-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="06780-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

