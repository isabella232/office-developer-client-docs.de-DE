---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428767"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="f6929-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="f6929-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="f6929-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6929-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6929-105">Bietet Zugriff auf die Anbietertabelle, eine Auflistung der Dienstanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="f6929-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f6929-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6929-106">Parameters</span></span>

 <span data-ttu-id="f6929-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6929-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f6929-108">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="f6929-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="f6929-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f6929-109">_lppTable_</span></span>
  
> <span data-ttu-id="f6929-110">[out] Ein Zeiger auf einen Zeiger auf die Anbietertabelle.</span><span class="sxs-lookup"><span data-stu-id="f6929-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6929-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6929-111">Return value</span></span>

<span data-ttu-id="f6929-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6929-112">S_OK</span></span> 
  
> <span data-ttu-id="f6929-113">Die Anbietertabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6929-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6929-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6929-114">Remarks</span></span>

<span data-ttu-id="f6929-115">Die **IMsgServiceAdmin::GetProviderTable-Methode** bietet Zugriff auf die MAPI-Anbietertabelle, eine Tabelle, in der alle derzeit im Profil installierten Adressbuch-, Nachrichtenspeicher- und Transportanbieter aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f6929-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="f6929-116">Im Gegensatz zur über die [IProviderAdmin::GetProviderTable-Methode](iprovideradmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die über **IMsgServiceAdmin::GetProviderTable** zurückgegebene Anbietertabelle keine zusätzlichen Zeilen enthalten, die Informationen darstellen, die einem oder mehreren Dienstanbietern im Profil zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6929-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="f6929-117">Anbieter, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Anbietertabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6929-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="f6929-118">Anbietertabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Profil nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f6929-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="f6929-119">Wenn das Profil keine Anbieter enthält, gibt **GetProviderTable** eine Tabelle mit null Zeilen und dem Rückgabewert S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f6929-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="f6929-120">Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f6929-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6929-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f6929-121">Notes to callers</span></span>

<span data-ttu-id="f6929-122">Verwenden Sie das folgende Verfahren, um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen:</span><span class="sxs-lookup"><span data-stu-id="f6929-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="f6929-123">Rufen Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) auf, um eine Eigenschaftseinschränkung aufzuerzwingen, die der **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) -Eigenschaft mit MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="f6929-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="f6929-124">Rufen Sie die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) auf, um die Tabelle nach der Spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="f6929-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="f6929-125">Rufen Sie [die IMAPITable::QueryRows-Methode](imapitable-queryrows.md) auf, um die Zeilen der Tabelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6929-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="f6929-126">Eine Alternative zu diesen Aufrufen besteht in einem einzigen Aufruf der [HrQueryAllRows-Funktion,](hrqueryallrows.md) bei dem alle entsprechenden Datenstrukturen übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6929-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="f6929-127">Wenn Sie die **spalten PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) in jeder Zeile abrufen, können Sie dieses Array von **MAPIUID-Strukturen** verwenden, um die Transportreihenfolge in einem Aufruf von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6929-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="f6929-128">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ führt folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="f6929-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="f6929-129">Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Spalten der Anbietertabelle von der [IMAPITable::QueryColumns-Methode zurückgegeben](imapitable-querycolumns.md) werden.</span><span class="sxs-lookup"><span data-stu-id="f6929-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="f6929-130">Die anfänglichen aktiven Spalten für eine Anbietertabelle sind die Spalten, die die **QueryColumns-Methode** zurückgibt, bevor der Anbieter, der die Tabelle enthält, die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="f6929-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="f6929-131">Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Zeilen der Anbietertabelle von **QueryRows zurückgegeben werden.**</span><span class="sxs-lookup"><span data-stu-id="f6929-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="f6929-132">Die ersten aktiven Zeilen für eine Anbietertabelle sind die Zeilen, die **QueryRows** vor dem Anbieter zurückgibt, der die Tabelle enthält, aufruft **SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="f6929-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="f6929-133">Steuert die Eigenschaftstypen der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird, bevor der Client, der die Anbietertabelle enthält, die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="f6929-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f6929-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6929-134">See also</span></span>



[<span data-ttu-id="f6929-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="f6929-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="f6929-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="f6929-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="f6929-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="f6929-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="f6929-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6929-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

