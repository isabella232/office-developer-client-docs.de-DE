---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411876"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="e74a5-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="e74a5-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="e74a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e74a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e74a5-105">Gibt eine Tabelle mit einmal erstellten Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e74a5-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e74a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e74a5-106">Parameters</span></span>

 <span data-ttu-id="e74a5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e74a5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e74a5-108">[in] Eine Bitmaske mit Flags, die den Typ von Zeichenfolgenspalten steuert, die in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e74a5-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="e74a5-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e74a5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e74a5-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e74a5-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e74a5-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e74a5-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="e74a5-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e74a5-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="e74a5-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e74a5-113">_lppTable_</span></span>
  
> <span data-ttu-id="e74a5-114">[out] Ein Zeiger auf einen Zeiger auf die einmal aufgeführte Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e74a5-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e74a5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e74a5-115">Return value</span></span>

<span data-ttu-id="e74a5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e74a5-116">S_OK</span></span> 
  
> <span data-ttu-id="e74a5-117">Die einmal aufgeführte Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e74a5-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="e74a5-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e74a5-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e74a5-119">Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="e74a5-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="e74a5-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e74a5-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e74a5-121">Der Adressbuchanbieter stellt keine einmal verwendeten Vorlagen bereit.</span><span class="sxs-lookup"><span data-stu-id="e74a5-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e74a5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e74a5-122">Remarks</span></span>

<span data-ttu-id="e74a5-123">MAPI ruft die **GetOneOffTable-Methode** auf, um einmal verfügbare Vorlagen zum Erstellen von Empfängern zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="e74a5-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="e74a5-124">Die neuen Empfänger werden der Empfängerliste einer ausgehenden Nachricht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e74a5-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="e74a5-125">Adressbuchanbieter sollten Benachrichtigungen in ihrer einmal erstellten Tabelle unterstützen, um MAPI über Vorlagenänderungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="e74a5-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="e74a5-126">MAPI hält die einmal aufgeführte Tabelle offen, um dynamische Aktualisierungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e74a5-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="e74a5-127">Adressbuchanbieter können auch eine einzelne Tabelle für jeden container unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e74a5-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="e74a5-128">Aufrufer rufen diese einmaltabelle ab, indem sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers aufrufen und die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft anfordern.</span><span class="sxs-lookup"><span data-stu-id="e74a5-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="e74a5-129">Die in dieser Tabelle verfügbaren Vorlagen werden zum Hinzufügen von Empfängern zum Container verwendet.</span><span class="sxs-lookup"><span data-stu-id="e74a5-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="e74a5-130">Eine Diskussion über die Unterschiede zwischen den beiden Arten von einmal erstellten Tabellen finden Sie unter [Implementing One-Off Tables](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e74a5-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="e74a5-131">Eine Liste der erforderlichen Spalten in der Einmaltabelle eines Adressbuchanbieters finden Sie unter [One-Off Tables](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e74a5-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e74a5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e74a5-132">See also</span></span>



[<span data-ttu-id="e74a5-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="e74a5-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="e74a5-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="e74a5-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="e74a5-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="e74a5-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="e74a5-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e74a5-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

