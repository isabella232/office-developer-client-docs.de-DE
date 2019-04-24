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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316602"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="4cd50-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="4cd50-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="4cd50-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cd50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cd50-105">Änderungen an einem Abschnitt des Nachrichtenspeicher Profils bleiben permanent.</span><span class="sxs-lookup"><span data-stu-id="4cd50-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4cd50-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd50-106">Parameters</span></span>

 <span data-ttu-id="4cd50-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cd50-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4cd50-108">in Eine Bitmaske von Flags, die den Typ des Nachrichtenspeichers angibt.</span><span class="sxs-lookup"><span data-stu-id="4cd50-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="4cd50-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4cd50-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4cd50-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="4cd50-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="4cd50-111">Der Nachrichtenspeicher ist temporär und sollte nicht der Nachrichtenspeichertabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4cd50-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="4cd50-112">Wenn MDB_TEMPORARY festgelegt ist, gibt **MODIFYPROFILE** S_OK sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="4cd50-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4cd50-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cd50-113">Return value</span></span>

<span data-ttu-id="4cd50-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cd50-114">S_OK</span></span> 
  
> <span data-ttu-id="4cd50-115">Die Änderungen am Profil Abschnitt waren erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4cd50-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cd50-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cd50-116">Remarks</span></span>

<span data-ttu-id="4cd50-117">Die **IMAPISupport:: ModifyProfile** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="4cd50-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="4cd50-118">Nachrichtenspeicher Anbieter rufen **ModifyProfile** auf, um MAPI aufzufordern, Ihre Profilinformationen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4cd50-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="4cd50-119">**ModifyProfile** fügt den dem anrufenden Anbieter zugeordneten Profil Abschnitt der Liste der installierten Ressourcen des Nachrichtenspeicher Anbieters hinzu.</span><span class="sxs-lookup"><span data-stu-id="4cd50-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="4cd50-120">Dies führt dazu, dass der Nachrichtenspeicher in der Nachrichtenspeichertabelle aufgeführt wird, die Clients über die [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zur Verfügung steht, und die geöffnet werden soll, ohne dass ein Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4cd50-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="4cd50-121">Wenn das MDB_TEMPORARY-Flag festgelegt ist, bewirkt MAPI nichts, und die Methode gibt sofort mit S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4cd50-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4cd50-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd50-122">See also</span></span>



[<span data-ttu-id="4cd50-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="4cd50-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="4cd50-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4cd50-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

