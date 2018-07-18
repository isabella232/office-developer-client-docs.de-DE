---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792360"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="56e7a-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="56e7a-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="56e7a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56e7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56e7a-105">Gibt einen Zeiger auf die einmaligen MAPI-Tabelle (eine Liste der Vorlagen, dass alle Anbieter für die Unterstützung für das Erstellen von neuen Empfänger Adressbuch).</span><span class="sxs-lookup"><span data-stu-id="56e7a-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="56e7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e7a-106">Parameters</span></span>

 <span data-ttu-id="56e7a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56e7a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="56e7a-108">[in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgenspalten steuert.</span><span class="sxs-lookup"><span data-stu-id="56e7a-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="56e7a-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="56e7a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="56e7a-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="56e7a-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="56e7a-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="56e7a-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="56e7a-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="56e7a-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="56e7a-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="56e7a-113">_lppTable_</span></span>
  
> <span data-ttu-id="56e7a-114">[out] Ein Zeiger auf einen Zeiger auf die einmaligen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="56e7a-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56e7a-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="56e7a-115">Return value</span></span>

<span data-ttu-id="56e7a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="56e7a-116">S_OK</span></span> 
  
> <span data-ttu-id="56e7a-117">Die einmalige Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="56e7a-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56e7a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e7a-118">Remarks</span></span>

<span data-ttu-id="56e7a-119">Die **IMAPISupport::GetOneOffTable** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="56e7a-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="56e7a-120">Von adressbuchanbietern implementierte Aufrufen **GetOneOffTable** , um die vollständige Liste der Vorlagen zum Erstellen von neuen Empfänger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="56e7a-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="56e7a-121">Die folgende Tabelle enthält Vorlagen, die Unterstützung von adressbuchanbietern implementierte, die in der Sitzung aktiv sind, sowie Formularvorlagen, die MAPI unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56e7a-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="56e7a-122">Die neu erstellten Empfänger können verwendet werden, um eine Nachricht oder ein Adressbuchcontainer hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="56e7a-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="56e7a-123">Eine Liste der Eigenschaften, die die erforderliche Spalte festlegen in einmaligen Tabellen bilden, finden Sie unter [Einmaligen Tabellen](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="56e7a-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="56e7a-124">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="56e7a-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="56e7a-125">Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56e7a-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="56e7a-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="56e7a-126">Notes to callers</span></span>

<span data-ttu-id="56e7a-127">Wenn Sie Erhalt von Benachrichtigungen von Änderungen an dieser einmaligen Tabelle registriert sind, erhalten Sie auch Benachrichtigungen von Änderungen an andere Anbieter einmaligen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="56e7a-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="56e7a-128">Basierend auf diese Benachrichtigungen, können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="56e7a-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56e7a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e7a-129">See also</span></span>



[<span data-ttu-id="56e7a-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="56e7a-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="56e7a-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="56e7a-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="56e7a-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56e7a-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="56e7a-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="56e7a-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="56e7a-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="56e7a-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="56e7a-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="56e7a-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="56e7a-136">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="56e7a-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="56e7a-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56e7a-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="56e7a-138">Einmalige Tabellen</span><span class="sxs-lookup"><span data-stu-id="56e7a-138">One-Off Tables</span></span>](one-off-tables.md)

