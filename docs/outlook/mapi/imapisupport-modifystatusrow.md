---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316642"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="986aa-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="986aa-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="986aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="986aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="986aa-105">Ändert die Statustabelle, indem eine neue Zeile hinzugefügt oder eine vorhandene Zeile geändert wird.</span><span class="sxs-lookup"><span data-stu-id="986aa-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="986aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="986aa-106">Parameters</span></span>

 <span data-ttu-id="986aa-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="986aa-107">_cValues_</span></span>
  
> <span data-ttu-id="986aa-108">in Die Anzahl der Eigenschaften, die in die neue oder geänderte Statustabellen Zeile eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="986aa-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="986aa-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="986aa-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="986aa-110">in Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die als Spalten in die neue oder geänderte Statustabellen Zeile eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="986aa-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="986aa-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="986aa-111">_ulFlags_</span></span>
  
> <span data-ttu-id="986aa-112">in Eine Bitmaske von Flags, die steuert, wie Informationen, die die Statustabellen Zeile definieren, verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="986aa-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="986aa-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="986aa-113">The following flag can be set:</span></span>
    
<span data-ttu-id="986aa-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="986aa-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="986aa-115">Weist MAPI an, die Eigenschaften, die im Array enthalten sind, von _lpColumnVals_ mit einer vorhandenen Statustabellen Zeile anstatt in einer neuen Zeile zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="986aa-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="986aa-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="986aa-116">Return value</span></span>

<span data-ttu-id="986aa-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="986aa-117">S_OK</span></span> 
  
> <span data-ttu-id="986aa-118">Die Statustabelle wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="986aa-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="986aa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="986aa-119">Remarks</span></span>

<span data-ttu-id="986aa-120">Die **IMAPISupport:: ModifyStatusRow** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="986aa-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="986aa-121">Dienstanbieter rufen **ModifyStatusRow** bei der Anmeldung auf, um der Statustabelle und zu anderen Zeiten während der Sitzung eine Zeile hinzuzufügen, um die Zeile zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="986aa-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="986aa-122">**ModifyStatusRow** bietet MAPI die zum Erstellen der Statustabelle erforderlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="986aa-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="986aa-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="986aa-123">Notes to callers</span></span>

<span data-ttu-id="986aa-124">Legen Sie das STATUSROW_UPDATE-Flag fest, wenn Sie **ModifyStatusRow** aufrufen, um Änderungen an den Eigenschaften in der vorhandenen Statustabellen Zeile vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="986aa-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="986aa-125">Auf diese Weise wird MAPI darüber informiert, dass nur die geänderten Spalten an den _lpColumnVals_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="986aa-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="986aa-126">Clients können die Informationen in der Statustabelle verwenden, um auf Ihr Status-Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="986aa-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="986aa-127">Eine vollständige Liste der Spalten, die Sie in die Statustabellen Zeile aufnehmen sollten, finden Sie unter [Statustabellen](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="986aa-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="986aa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="986aa-128">See also</span></span>



[<span data-ttu-id="986aa-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="986aa-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

