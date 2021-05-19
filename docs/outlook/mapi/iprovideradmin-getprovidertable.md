---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434473"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="aa772-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="aa772-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="aa772-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa772-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa772-105">Bietet Zugriff auf die Anbietertabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="aa772-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="aa772-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa772-106">Parameters</span></span>

 <span data-ttu-id="aa772-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa772-107">_ulFlags_</span></span>
  
> <span data-ttu-id="aa772-108">[in] Eine Bitmaske mit Flags, die den Typ der in den Spalten der Anbietertabelle zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="aa772-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="aa772-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="aa772-109">The following flag can be set:</span></span>
    
<span data-ttu-id="aa772-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aa772-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aa772-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="aa772-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="aa772-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Spalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="aa772-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="aa772-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="aa772-113">_lppTable_</span></span>
  
> <span data-ttu-id="aa772-114">[out] Ein Zeiger auf einen Zeiger auf die Anbietertabelle.</span><span class="sxs-lookup"><span data-stu-id="aa772-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa772-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa772-115">Return value</span></span>

<span data-ttu-id="aa772-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa772-116">S_OK</span></span> 
  
> <span data-ttu-id="aa772-117">Die Anbietertabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa772-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa772-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa772-118">Remarks</span></span>

<span data-ttu-id="aa772-119">Die **IProviderAdmin::GetProviderTable-Methode** ruft einen Zeiger auf die Anbietertabelle des Nachrichtendiensts ab, eine Tabelle, die MAPI verwaltet, die Informationen zu den einzelnen Dienstanbietern im Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="aa772-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="aa772-120">Im Gegensatz zur von der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die von **IProviderAdmin::GetProviderTable** zurückgegebene Anbietertabelle zusätzliche Zeilen enthalten, die Informationen darstellen, die einem oder mehreren Dienstanbietern im Nachrichtendienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aa772-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="aa772-121">Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" der Datei Mapisvc.inf hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aa772-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="aa772-122">Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, speichert er die **MAPIUID-Strukturen** für diese Abschnitte in der **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aa772-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="aa772-123">**PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Nachrichtendienstprofil gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aa772-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="aa772-124">Anbieter, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Anbietertabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa772-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="aa772-125">Anbietertabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Nachrichtendienst nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aa772-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="aa772-126">Wenn der Nachrichtendienst über keine Anbieter verfügt, gibt **IProviderAdmin::GetProviderTable** eine Tabelle mit null Zeilen und dem Rückgabewert S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="aa772-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="aa772-127">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa772-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="aa772-128">Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="aa772-129">Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="aa772-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa772-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="aa772-130">Notes to callers</span></span>

<span data-ttu-id="aa772-131">Um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen, sortieren Sie die Tabelle nach der spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa772-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="aa772-132">Um nur die Zeilen abzurufen, die Dienstanbieter darstellen (ohne zusätzliche Zeilen), beschränken Sie den Abruf auf die Zeilen, die den Wert PT_ERROR in der Spalte **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) haben.</span><span class="sxs-lookup"><span data-stu-id="aa772-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa772-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="aa772-133">MFCMAPI reference</span></span>

<span data-ttu-id="aa772-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="aa772-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa772-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="aa772-135">**File**</span></span>|<span data-ttu-id="aa772-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="aa772-136">**Function**</span></span>|<span data-ttu-id="aa772-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="aa772-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aa772-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aa772-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="aa772-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="aa772-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="aa772-140">MFCMAPI verwendet die **IProviderAdmin::GetProviderTable-Methode,** um die Tabelle der Anbieter zum Rendern in einem neuen Dialogfeld zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aa772-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa772-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa772-141">See also</span></span>



[<span data-ttu-id="aa772-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="aa772-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="aa772-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="aa772-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="aa772-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="aa772-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="aa772-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="aa772-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="aa772-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="aa772-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="aa772-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa772-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="aa772-148">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="aa772-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

