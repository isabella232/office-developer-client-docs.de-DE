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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792373"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="cab15-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="cab15-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="cab15-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cab15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cab15-105">Ändert eine Nachricht Profilabschnitt permanent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cab15-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cab15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cab15-106">Parameters</span></span>

 <span data-ttu-id="cab15-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cab15-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cab15-108">[in] Eine Bitmaske aus Flags, die den Typ der Nachricht gibt an, speichern.</span><span class="sxs-lookup"><span data-stu-id="cab15-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="cab15-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cab15-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cab15-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="cab15-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="cab15-111">Der Nachrichtenspeicher ist vorübergehend und sollten nicht auf die Nachricht Store-Tabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cab15-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="cab15-112">Wenn MDB_TEMPORARY festgelegt ist, gibt **ModifyProfile** sofort S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="cab15-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cab15-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="cab15-113">Return value</span></span>

<span data-ttu-id="cab15-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="cab15-114">S_OK</span></span> 
  
> <span data-ttu-id="cab15-115">Die Änderungen in den Profilabschnitt waren erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cab15-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cab15-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cab15-116">Remarks</span></span>

<span data-ttu-id="cab15-117">Die **IMAPISupport::ModifyProfile** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="cab15-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="cab15-118">E-Mail-Speicher-Anbieter Aufruf **ModifyProfile** auffordern, MAPI, um ihre Profilinformationen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cab15-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="cab15-119">**ModifyProfile** fügt Abschnitts Profile, die der aufrufende Anbieter zur Liste der installierten Nachricht Store Anbieter Ressourcen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cab15-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="cab15-120">Daraufhin wird den Nachrichtenspeicher in der Nachricht Store-Tabelle aufgelistet werden die Clients durch die [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zur Verfügung steht, und ohne die Anzeige von einem Dialogfeld geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cab15-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="cab15-121">Wenn das Flag MDB_TEMPORARY festgelegt ist, MAPI hat keine Auswirkung, und die Methode gibt sofort mit S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="cab15-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cab15-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cab15-122">See also</span></span>



[<span data-ttu-id="cab15-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="cab15-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="cab15-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cab15-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

