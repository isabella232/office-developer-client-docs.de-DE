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
ms.openlocfilehash: 834b010dc4810e26264bb418de9630bc83b99810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565291"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="0cd5e-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="0cd5e-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="0cd5e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cd5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cd5e-105">Bietet Zugriff auf die Tabelle Dienstanbieter, eine Liste der Dienstanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="0cd5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cd5e-106">Parameters</span></span>

 <span data-ttu-id="0cd5e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0cd5e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0cd5e-108">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="0cd5e-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="0cd5e-109">_lppTable_</span></span>
  
> <span data-ttu-id="0cd5e-110">[out] Ein Zeiger auf einen Zeiger auf den Anbieter-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0cd5e-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0cd5e-111">Return value</span></span>

<span data-ttu-id="0cd5e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0cd5e-112">S_OK</span></span> 
  
> <span data-ttu-id="0cd5e-113">Die Anbieter Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0cd5e-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0cd5e-114">Remarks</span></span>

<span data-ttu-id="0cd5e-115">Die **IMsgServiceAdmin::GetProviderTable** -Methode ermöglicht den Zugriff auf die MAPI-Anbieter-Tabelle eine Tabelle, die alle Adressbuch, Nachrichtenspeicher und Transportanbieter, die derzeit im Profil installiert aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="0cd5e-116">Im Gegensatz zu der Tabelle der Dienstanbieter über die [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) -Methode zurückgegeben kann nicht die Anbieter zurückgegebenen **IMsgServiceAdmin::GetProviderTable** zusätzliche Zeilen einzubeziehen, die Informationen im Zusammenhang darstellen mit mindestens -Dienstanbietern im Profil</span><span class="sxs-lookup"><span data-stu-id="0cd5e-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="0cd5e-117">Anbieter, die gelöscht wurden, oder verwendet werden, doch zum Löschen markiert wurden, sind nicht in der Provider-Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="0cd5e-118">Provider-Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschvorgänge aus dem Profil in der Tabelle nicht wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="0cd5e-119">Wenn das Profil keine Anbieter aufweist, gibt **GetProviderTable** eine Tabelle mit 0 (null) Zeilen und den Rückgabewert S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="0cd5e-120">Eine vollständige Liste der Spalten in der Tabelle Anbieter finden Sie unter [Provider-Tabelle](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0cd5e-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0cd5e-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0cd5e-121">Notes to callers</span></span>

<span data-ttu-id="0cd5e-122">Rufen Sie die Zeilen einer Tabelle Anbieter in Transport Reihenfolge verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0cd5e-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="0cd5e-123">Rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, um eine eigenschaftseinschränkung zugrunde liegen, die die **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))-Eigenschaft mit MAPI_TRANSPORT_PROVIDER entspricht.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="0cd5e-124">Aufrufen der [SortTable](imapitable-sorttable.md) -Methode, um die Tabelle nach der **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))-Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="0cd5e-125">Rufen Sie [die QueryRows, um die Zeilen der Tabelle zu erhalten](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="0cd5e-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="0cd5e-126">Eine Alternative zu diesen anrufen ist auf einen einzigen Aufruf der Funktion [HrQueryAllRows](hrqueryallrows.md) mit aller entsprechenden Daten ansetzen, die Strukturen in übergeben.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="0cd5e-127">Wenn Sie die Spalten **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) in den einzelnen Zeilen abrufen, können Sie dieses Array von **MAPIUID** -Strukturen, die Transport-Reihenfolge in einem Aufruf von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="0cd5e-128">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ bewirkt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0cd5e-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="0cd5e-129">Legt den Typ String in Unicode für von der [IMAPITable::QueryColumns](imapitable-querycolumns.md) -Methode für die anfänglichen aktiven Spalten der Tabelle vom Anbieter zurückgegebenen Daten fest.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="0cd5e-130">Die ersten aktiven Spalten für eine Tabelle Anbieter sind die Spalten, die die **QueryColumns** -Methode vor der Anbieter zurückgibt, die die Tabelle Aufrufe die [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="0cd5e-131">Legt den Typ String in Unicode für von **QueryRows**für die anfänglichen aktiven Zeilen der Tabelle vom Anbieter zurückgegebenen Daten fest.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="0cd5e-132">Die anfänglichen aktiven Zeilen, die für eine Anbieter-Tabelle sind die Zeilen, die **QueryRows** vor der Anbieter zurückgibt, das die Tabelle Aufrufe **SetColumns**enthält.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="0cd5e-133">Steuert die Eigenschaftentypen der Sortierreihenfolge von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben wird, bevor der Client, der die Anbieter-Tabelle enthält die [SortTable](imapitable-sorttable.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="0cd5e-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0cd5e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cd5e-134">See also</span></span>



[<span data-ttu-id="0cd5e-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="0cd5e-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="0cd5e-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="0cd5e-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="0cd5e-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="0cd5e-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="0cd5e-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0cd5e-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

