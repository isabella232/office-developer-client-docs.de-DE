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
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="f4ea5-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f4ea5-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="f4ea5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4ea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4ea5-105">Gibt einen Zeiger auf die MAPI-einmalige Tabelle zurück (eine Liste von Vorlagen, die von allen Adressbuch Anbietern für das Erstellen neuer Empfänger unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="f4ea5-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f4ea5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4ea5-106">Parameters</span></span>

 <span data-ttu-id="f4ea5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4ea5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f4ea5-108">in Eine Bitmaske von Flags, die den Typ der Zeichenfolgenspalten steuert.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="f4ea5-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f4ea5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f4ea5-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4ea5-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f4ea5-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f4ea5-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="f4ea5-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f4ea5-113">_lppTable_</span></span>
  
> <span data-ttu-id="f4ea5-114">Out Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4ea5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4ea5-115">Return value</span></span>

<span data-ttu-id="f4ea5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4ea5-116">S_OK</span></span> 
  
> <span data-ttu-id="f4ea5-117">Die einmalige Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4ea5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4ea5-118">Remarks</span></span>

<span data-ttu-id="f4ea5-119">Die **IMAPISupport:: GetOneOffTable** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="f4ea5-120">Adressbuchanbieter rufen **GetOneOffTable** auf, um die vollständige Liste der Vorlagen zum Erstellen neuer Empfänger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="f4ea5-121">Diese Tabelle enthält Vorlagen für Adressbuchanbieter, die in der Sitzungsunterstützung aktiv sind, sowie Vorlagen, die von MAPI unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="f4ea5-122">Die neu erstellten Empfänger können verwendet werden, um eine Nachricht zu adressieren oder einem Adressbuchcontainer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="f4ea5-123">Eine Liste der Eigenschaften, die den erforderlichen Spaltensatz in einmaligen Tabellen bilden, finden Sie unter [einmalige Tabellen](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f4ea5-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="f4ea5-124">Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="f4ea5-125">Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4ea5-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f4ea5-126">Notes to callers</span></span>

<span data-ttu-id="f4ea5-127">Wenn Sie für den Erhalt von Benachrichtigungen über Änderungen an dieser einmaligen Tabelle registriert sind, erhalten Sie auch Benachrichtigungen über Änderungen an den einmaligen Tabellen anderer Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="f4ea5-128">Basierend auf diesen Benachrichtigungen können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f4ea5-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4ea5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4ea5-129">See also</span></span>



[<span data-ttu-id="f4ea5-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f4ea5-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="f4ea5-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="f4ea5-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="f4ea5-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4ea5-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="f4ea5-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="f4ea5-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="f4ea5-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f4ea5-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f4ea5-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="f4ea5-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="f4ea5-136">Kanonische Pidtagcreatetemplates (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4ea5-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="f4ea5-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4ea5-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="f4ea5-138">Einmalige Tabellen</span><span class="sxs-lookup"><span data-stu-id="f4ea5-138">One-Off Tables</span></span>](one-off-tables.md)

