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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412758"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="1db06-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="1db06-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="1db06-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1db06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1db06-105">Gibt einen Zeiger auf die einmal aufgeführte MAPI-Tabelle zurück (eine Liste der Vorlagen, die von allen Adressbuchanbietern zum Erstellen neuer Empfänger unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="1db06-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1db06-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1db06-106">Parameters</span></span>

 <span data-ttu-id="1db06-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1db06-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1db06-108">[in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolgenspalten steuert.</span><span class="sxs-lookup"><span data-stu-id="1db06-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="1db06-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1db06-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1db06-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1db06-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1db06-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="1db06-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="1db06-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="1db06-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="1db06-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1db06-113">_lppTable_</span></span>
  
> <span data-ttu-id="1db06-114">[out] Ein Zeiger auf einen Zeiger auf die einmal aufgeführte Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1db06-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1db06-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1db06-115">Return value</span></span>

<span data-ttu-id="1db06-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1db06-116">S_OK</span></span> 
  
> <span data-ttu-id="1db06-117">Die einmal aufgeführte Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1db06-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1db06-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1db06-118">Remarks</span></span>

<span data-ttu-id="1db06-119">Die **IMAPISupport::GetOneOffTable-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="1db06-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="1db06-120">Adressbuchanbieter rufen **GetOneOffTable auf,** um die vollständige Liste der Vorlagen zum Erstellen neuer Empfänger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1db06-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="1db06-121">Diese Tabelle enthält Vorlagen für Adressbuchanbieter, die in der Sitzungsunterstützung aktiv sind, sowie Vorlagen, die MAPI unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1db06-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="1db06-122">Die neu erstellten Empfänger können verwendet werden, um eine Nachricht zu adressiert oder einem Adressbuchcontainer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1db06-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="1db06-123">Eine Liste der Eigenschaften, aus der die erforderliche Spaltensatz in einmal festgelegten Tabellen ist, finden Sie unter [One-Off Tables](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1db06-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="1db06-124">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1db06-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="1db06-125">Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird.</span><span class="sxs-lookup"><span data-stu-id="1db06-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1db06-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1db06-126">Notes to callers</span></span>

<span data-ttu-id="1db06-127">Wenn Sie registriert sind, um Benachrichtigungen über Änderungen an dieser einmal erstellten Tabelle zu erhalten, erhalten Sie auch Benachrichtigungen über Änderungen an den einmal aufgeführten Tabellen anderer Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1db06-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="1db06-128">Basierend auf diesen Benachrichtigungen können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1db06-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1db06-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1db06-129">See also</span></span>



[<span data-ttu-id="1db06-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="1db06-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="1db06-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="1db06-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="1db06-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1db06-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="1db06-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1db06-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="1db06-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1db06-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1db06-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="1db06-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="1db06-136">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1db06-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="1db06-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1db06-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="1db06-138">Einmaltabellen</span><span class="sxs-lookup"><span data-stu-id="1db06-138">One-Off Tables</span></span>](one-off-tables.md)

