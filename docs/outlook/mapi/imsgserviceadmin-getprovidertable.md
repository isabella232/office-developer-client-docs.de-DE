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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317381"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="edf4e-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="edf4e-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="edf4e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edf4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edf4e-105">Ermöglicht den Zugriff auf die Anbieter Tabelle, eine Liste der Dienstanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="edf4e-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="edf4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edf4e-106">Parameters</span></span>

 <span data-ttu-id="edf4e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edf4e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="edf4e-108">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="edf4e-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="edf4e-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="edf4e-109">_lppTable_</span></span>
  
> <span data-ttu-id="edf4e-110">Out Ein Zeiger auf einen Zeiger auf die Anbieter Tabelle.</span><span class="sxs-lookup"><span data-stu-id="edf4e-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edf4e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edf4e-111">Return value</span></span>

<span data-ttu-id="edf4e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="edf4e-112">S_OK</span></span> 
  
> <span data-ttu-id="edf4e-113">Die Anbieter Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="edf4e-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edf4e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edf4e-114">Remarks</span></span>

<span data-ttu-id="edf4e-115">Die **IMsgServiceAdmin:: GetProvider** Table-Methode ermöglicht den Zugriff auf die MAPI-Anbieter Tabelle, eine Tabelle, in der das gesamte Adressbuch, der Nachrichtenspeicher und die Transportanbieter aufgelistet sind, die aktuell im Profil installiert sind.</span><span class="sxs-lookup"><span data-stu-id="edf4e-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="edf4e-116">Im Gegensatz zur Anbieter Tabelle, die über die [IProviderAdmin:: GetProvider](iprovideradmin-getprovidertable.md) Table-Methode zurückgegeben wird, kann die durch **IMsgServiceAdmin::** getproviderable zurückgegebene Anbieter Tabelle keine zusätzlichen Zeilen mit zugeordneten Informationen darstellen. mit einem oder mehreren Dienstanbietern im Profil.</span><span class="sxs-lookup"><span data-stu-id="edf4e-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="edf4e-117">Anbieter, die gelöscht oder verwendet wurden, aber zum Löschen markiert wurden, sind nicht in der Anbieter Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="edf4e-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="edf4e-118">Anbieter Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Profil nicht in der Tabelle wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edf4e-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="edf4e-119">Wenn das Profil keine Anbieter hat, \*\*\*\* gibt getproviderable eine Tabelle mit null Zeilen und dem RÜCKGABEwert S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="edf4e-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="edf4e-120">Eine vollständige Liste der Spalten in der Anbieter Tabelle finden Sie unter [Provider Table](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="edf4e-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="edf4e-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="edf4e-121">Notes to callers</span></span>

<span data-ttu-id="edf4e-122">Gehen Sie folgendermaßen vor, um die Zeilen einer Anbieter Tabelle in der Transport Reihenfolge abzurufen:</span><span class="sxs-lookup"><span data-stu-id="edf4e-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="edf4e-123">Rufen Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode auf, um eine Eigenschaftseinschränkung aufzuerlegen, die der **PR_RESOURCE_TYPE** ([PIDTAGRESOURCETYPE (](pidtagresourcetype-canonical-property.md))-Eigenschaft mit MAPI_TRANSPORT_PROVIDER entspricht.</span><span class="sxs-lookup"><span data-stu-id="edf4e-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="edf4e-124">Rufen Sie die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode auf, um die Tabelle nach der **PR_PROVIDER_ORDINAL** ([pidtagproviderordinal (](pidtagproviderordinal-canonical-property.md))-Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="edf4e-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="edf4e-125">Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode auf, um die Zeilen der Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="edf4e-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="edf4e-126">Eine Alternative zu diesen Aufrufen besteht darin, einen einzelnen Aufruf der [HrQueryAllRows](hrqueryallrows.md) -Funktion mit allen entsprechenden Datenstrukturen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="edf4e-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="edf4e-127">Wenn Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalten in den einzelnen Zeilen abrufen, können Sie dieses Array von **MAPIUID** -Strukturen zum Festlegen der Transport Reihenfolge in einem Aufruf von [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="edf4e-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="edf4e-128">Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter führt zu folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="edf4e-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="edf4e-129">Legt den Zeichenfolgentyp für Daten fest, die für die anfänglichen aktiven Spalten der Anbieter Tabelle von der [IMAPITable:: QueryColumns](imapitable-querycolumns.md) -Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edf4e-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="edf4e-130">Die ersten aktiven Spalten für eine Anbieter Tabelle sind die Spalten, die die **QueryColumns** -Methode zurückgibt, bevor der Anbieter, der die Tabelle enthält, die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="edf4e-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="edf4e-131">Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Zeilen der Anbieter Tabelle von **QueryRows**zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edf4e-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="edf4e-132">Die ersten aktiven Zeilen für eine Anbieter Tabelle sind die Zeilen, die **QueryRows** zurückgibt, bevor der Anbieter, der die Tabelle enthält, SetColumns aufruft. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="edf4e-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="edf4e-133">Steuert die Eigenschaftentypen der Sortierreihenfolge, die von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben wird, bevor der Client, der die Anbieter Tabelle enthält, die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="edf4e-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="edf4e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edf4e-134">See also</span></span>



[<span data-ttu-id="edf4e-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="edf4e-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="edf4e-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="edf4e-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="edf4e-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="edf4e-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="edf4e-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edf4e-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

