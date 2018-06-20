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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 24718c50d02da5d60a6594f56ea6100650fe9f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792371"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="7867a-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="7867a-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="7867a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7867a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7867a-105">Ändert die Statustabelle durch eine neue Zeile hinzufügen oder Ändern einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="7867a-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7867a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7867a-106">Parameters</span></span>

 <span data-ttu-id="7867a-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7867a-107">_cValues_</span></span>
  
> <span data-ttu-id="7867a-108">[in] Die Anzahl der Eigenschaften in die neue oder geänderte Status Tabellenzeile enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7867a-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="7867a-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="7867a-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="7867a-110">[in] Ein Zeiger auf ein Array der Eigenschaftswerte, die beschreiben die Eigenschaften als Spalten in der neuen oder geänderten Status Tabellenzeile eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7867a-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="7867a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7867a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="7867a-112">[in] Eine Bitmaske aus Flags, die steuert, wie Informationen, die die Status Tabellenzeile definieren verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="7867a-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="7867a-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7867a-113">The following flag can be set:</span></span>
    
<span data-ttu-id="7867a-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7867a-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="7867a-115">Weist das MAPI zum Zusammenführen der Eigenschaften im Array auf den _LpColumnVals_ mit einer vorhandenen Tabelle Statuszeile, statt die Daten in eine neue Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="7867a-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7867a-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7867a-116">Return value</span></span>

<span data-ttu-id="7867a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="7867a-117">S_OK</span></span> 
  
> <span data-ttu-id="7867a-118">Die Statustabelle wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7867a-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7867a-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7867a-119">Remarks</span></span>

<span data-ttu-id="7867a-120">Die **IMAPISupport::ModifyStatusRow** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="7867a-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="7867a-121">Dienstanbieter rufen **ModifyStatusRow** Sie bei der Anmeldung, um die Statustabelle eine Zeile hinzuzufügen und zu anderen Zeiten während der Sitzung auf die Zeile zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7867a-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="7867a-122">**ModifyStatusRow** bietet MAPI die erforderlichen Informationen für die Statustabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7867a-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7867a-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7867a-123">Notes to callers</span></span>

<span data-ttu-id="7867a-124">Legen Sie das STATUSROW_UPDATE-Flag beim Aufruf **ModifyStatusRow** so ändern Sie die Eigenschaften in Ihrer vorhandenen Status Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="7867a-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="7867a-125">Auf diese Weise informiert MAPI an, dass nur die Spalten, die geändert wird im _LpColumnVals_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7867a-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="7867a-126">Clients können die Informationen in der Tabelle "Status" verwenden, den Zugriff auf Ihr Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="7867a-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="7867a-127">Eine vollständige Liste der Spalten, die in der Statuszeile Tabelle aufgenommen werden sollen, finden Sie unter [Statustabellen](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7867a-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7867a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7867a-128">See also</span></span>



[<span data-ttu-id="7867a-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7867a-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

