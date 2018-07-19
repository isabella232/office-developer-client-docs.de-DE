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
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792857"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="be66a-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="be66a-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="be66a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be66a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be66a-105">Sendet eine Benachrichtigung für eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="be66a-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="be66a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be66a-106">Parameters</span></span>

 <span data-ttu-id="be66a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be66a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="be66a-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="be66a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="be66a-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="be66a-109">_cValues_</span></span>
  
> <span data-ttu-id="be66a-110">[in] Durch den Parameter _LpSPropValue_ auf zeigt die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="be66a-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="be66a-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="be66a-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="be66a-112">[in] Ein Zeiger auf eine **SPropValue** -Struktur, die die Werte der Spalten in der Zielzeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="be66a-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be66a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be66a-113">Return value</span></span>

<span data-ttu-id="be66a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="be66a-114">S_OK</span></span> 
  
> <span data-ttu-id="be66a-115">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="be66a-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be66a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be66a-116">Remarks</span></span>

<span data-ttu-id="be66a-117">Die **ITableData::HrNotify** -Methode sendet eine Benachrichtigung TABLE_ROW_MODIFIED für die Zeile, die mit die Zeile, die durch die Eigenschaften auf das durch den Parameter _LpSPropValue_ beschriebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="be66a-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="be66a-118">**HrNotify** sendet die Benachrichtigung, unabhängig davon, ob die Zeile geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="be66a-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="be66a-119">Alle Clients und -Dienstanbieter, die Ansichten für die Tabelle und [IMAPITable::Advise](imapitable-advise.md) zum Registrieren für Benachrichtigungen für ihre Ansichten aufgerufen haben erhalten diese Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="be66a-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be66a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be66a-120">See also</span></span>



[<span data-ttu-id="be66a-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="be66a-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="be66a-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="be66a-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="be66a-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be66a-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

