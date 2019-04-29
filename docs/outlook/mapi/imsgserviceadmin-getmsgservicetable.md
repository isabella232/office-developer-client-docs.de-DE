---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410476"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="37d73-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="37d73-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="37d73-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d73-105">Ermöglicht den Zugriff auf die Nachrichtendienst Tabelle, eine Liste der Nachrichtendienste im Profil.</span><span class="sxs-lookup"><span data-stu-id="37d73-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="37d73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37d73-106">Parameters</span></span>

 <span data-ttu-id="37d73-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37d73-107">_ulFlags_</span></span>
  
> <span data-ttu-id="37d73-108">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="37d73-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="37d73-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="37d73-109">_lppTable_</span></span>
  
> <span data-ttu-id="37d73-110">Out Ein Zeiger auf einen Zeiger auf die Nachrichtendienst Tabelle.</span><span class="sxs-lookup"><span data-stu-id="37d73-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37d73-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37d73-111">Return value</span></span>

<span data-ttu-id="37d73-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="37d73-112">S_OK</span></span> 
  
> <span data-ttu-id="37d73-113">Die Nachrichtendienst Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37d73-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37d73-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37d73-114">Remarks</span></span>

<span data-ttu-id="37d73-115">Die **IMsgServiceAdmin:: GetMsgServiceTable** -Methode ermöglicht den Zugriff auf die Nachrichtendienst Tabelle, eine Tabelle, die von MAPI verwaltet wird, die die im Sitzungsprofil installierten Nachrichtendienste auflistet.</span><span class="sxs-lookup"><span data-stu-id="37d73-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="37d73-116">Eine vollständige Liste der Spalten in der Tabelle "Nachrichtendienst" finden Sie unter [Message Service Table](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="37d73-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="37d73-117">Die Nachrichtendienst Tabelle ist statisch.</span><span class="sxs-lookup"><span data-stu-id="37d73-117">The message service table is static.</span></span> <span data-ttu-id="37d73-118">Nachdem ein Clientzugriff darauf erhalten hat, hat der nachfolgende Nachrichtendienst keine Auswirkungen darauf.</span><span class="sxs-lookup"><span data-stu-id="37d73-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="37d73-119">Wenn im aktuellen Profil keine Nachrichtendienste vorhanden sind, gibt **GetMsgServiceTable** eine Tabelle mit null Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="37d73-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37d73-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="37d73-120">MFCMAPI reference</span></span>

<span data-ttu-id="37d73-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="37d73-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37d73-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="37d73-122">**File**</span></span>|<span data-ttu-id="37d73-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="37d73-123">**Function**</span></span>|<span data-ttu-id="37d73-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="37d73-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37d73-125">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="37d73-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="37d73-126">CMsgServiceTableDlg:: OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="37d73-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="37d73-127">MFCMAPI verwendet die **IMsgServiceAdmin:: GetMsgServiceTable** -Methode, um die Tabelle mit Diensten in einem Profil zu laden, das in der Ansicht gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="37d73-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37d73-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37d73-128">See also</span></span>



[<span data-ttu-id="37d73-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="37d73-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="37d73-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="37d73-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="37d73-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37d73-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="37d73-132">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="37d73-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

