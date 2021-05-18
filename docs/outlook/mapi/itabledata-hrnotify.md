---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413269"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="3c8d8-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="3c8d8-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="3c8d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c8d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c8d8-105">Sendet eine Benachrichtigung für eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="3c8d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8d8-106">Parameters</span></span>

 <span data-ttu-id="3c8d8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3c8d8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3c8d8-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3c8d8-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="3c8d8-109">_cValues_</span></span>
  
> <span data-ttu-id="3c8d8-110">[in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die der  _lpSPropValue-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="3c8d8-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="3c8d8-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="3c8d8-112">[in] Ein Zeiger auf eine **SPropValue-Struktur,** die die Werte der Spalten in der Zielzeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c8d8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c8d8-113">Return value</span></span>

<span data-ttu-id="3c8d8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c8d8-114">S_OK</span></span> 
  
> <span data-ttu-id="3c8d8-115">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c8d8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c8d8-116">Remarks</span></span>

<span data-ttu-id="3c8d8-117">Die **ITableData::HrNotify-Methode** sendet eine TABLE_ROW_MODIFIED-Benachrichtigung für die Zeile, die der Zeile entspricht, die durch die Eigenschaften beschrieben wird, auf die der  _lpSPropValue-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="3c8d8-118">**HrNotify** sendet die Benachrichtigung, unabhängig davon, ob Änderungen an der Zeile vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="3c8d8-119">Alle Clients und Dienstanbieter, die über Ansichten der Tabelle verfügen und [IMAPITable::Advise](imapitable-advise.md) aufgerufen haben, sich für Benachrichtigungen in ihren Ansichten zu registrieren, erhalten diese Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="3c8d8-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c8d8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c8d8-120">See also</span></span>



[<span data-ttu-id="3c8d8-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3c8d8-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3c8d8-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3c8d8-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="3c8d8-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c8d8-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

