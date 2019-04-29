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
# <a name="iablogongetoneofftable"></a><span data-ttu-id="74423-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="74423-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="74423-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74423-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74423-105">Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74423-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="74423-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74423-106">Parameters</span></span>

 <span data-ttu-id="74423-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74423-107">_ulFlags_</span></span>
  
> <span data-ttu-id="74423-108">in Eine Bitmaske von Flags, die den Typ der Zeichenfolgenspalten in der Tabelle steuert.</span><span class="sxs-lookup"><span data-stu-id="74423-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="74423-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="74423-109">The following flag can be set:</span></span>
    
<span data-ttu-id="74423-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74423-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="74423-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="74423-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="74423-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="74423-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="74423-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="74423-113">_lppTable_</span></span>
  
> <span data-ttu-id="74423-114">Out Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74423-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74423-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74423-115">Return value</span></span>

<span data-ttu-id="74423-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="74423-116">S_OK</span></span> 
  
> <span data-ttu-id="74423-117">Die einmalige Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="74423-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="74423-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="74423-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="74423-119">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="74423-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="74423-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="74423-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="74423-121">Der Adressbuchanbieter liefert keine einmaligen Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="74423-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74423-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74423-122">Remarks</span></span>

<span data-ttu-id="74423-123">MAPI Ruft die **GetOneOffTable** -Methode auf, um für die Erstellung von Empfängern einmalige Vorlagen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="74423-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="74423-124">Die neuen Empfänger werden der Empfängerliste einer ausgehenden Nachricht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="74423-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="74423-125">Adressbuchanbieter sollten die Benachrichtigung über ihre einmalige Tabelle unterstützen, um MAPI über Vorlagenänderungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="74423-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="74423-126">MAPI hält die einmalige Tabelle geöffnet, um dynamische Updates zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="74423-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="74423-127">Adressbuchanbieter können auch eine einmalige Tabelle für jeden ihrer Container unterstützen.</span><span class="sxs-lookup"><span data-stu-id="74423-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="74423-128">Aufrufer rufen diese einmalige Tabelle ab, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers aufrufen und die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft anfordern.</span><span class="sxs-lookup"><span data-stu-id="74423-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="74423-129">Die über diese Tabelle verfügbaren Vorlagen werden zum Hinzufügen von Empfängern zum Container verwendet.</span><span class="sxs-lookup"><span data-stu-id="74423-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="74423-130">Eine Erläuterung der Unterschiede zwischen den beiden Arten von einmaligen Tabellen finden Sie unter [Implementieren von einmal Tabellen](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="74423-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="74423-131">Eine Liste der erforderlichen Spalten in der einmaligen Tabelle eines Adressbuch Anbieters finden Sie unter [einmalige Tabellen](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="74423-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74423-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74423-132">See also</span></span>



[<span data-ttu-id="74423-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="74423-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="74423-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="74423-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="74423-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="74423-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="74423-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74423-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

