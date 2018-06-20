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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792647"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="002fe-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="002fe-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="002fe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="002fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="002fe-105">Bietet Zugriff auf die Nachricht Service Tabelle eine Liste der Nachrichtendienste im Profil.</span><span class="sxs-lookup"><span data-stu-id="002fe-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="002fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="002fe-106">Parameters</span></span>

 <span data-ttu-id="002fe-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="002fe-107">_ulFlags_</span></span>
  
> <span data-ttu-id="002fe-108">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="002fe-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="002fe-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="002fe-109">_lppTable_</span></span>
  
> <span data-ttu-id="002fe-110">[out] Ein Zeiger auf einen Zeiger auf die Nachricht Service-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="002fe-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="002fe-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="002fe-111">Return value</span></span>

<span data-ttu-id="002fe-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="002fe-112">S_OK</span></span> 
  
> <span data-ttu-id="002fe-113">Die Tabelle der Dienste wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="002fe-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="002fe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="002fe-114">Remarks</span></span>

<span data-ttu-id="002fe-115">Die **IMsgServiceAdmin::GetMsgServiceTable** -Methode ermöglicht den Zugriff auf die Nachricht Service Tabelle eine Tabelle, die MAPI verwaltet, die Message-Dienste im Profil der Sitzung derzeit installiert aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="002fe-116">Eine vollständige Liste der Spalten in der Tabelle der Dienste finden Sie unter [Message Service-Tabelle](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="002fe-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="002fe-117">Die Tabelle der Dienste sind statisch.</span><span class="sxs-lookup"><span data-stu-id="002fe-117">The message service table is static.</span></span> <span data-ttu-id="002fe-118">Nachdem ein Client Zugriff darauf gewährt wurde, wirkt nachfolgende Meldung Dienst hinzufügen oder Löschen nicht sich.</span><span class="sxs-lookup"><span data-stu-id="002fe-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="002fe-119">Wenn keine Message-Dienste in das aktuelle Profil vorhanden sind, gibt **GetMsgServiceTable** eine Tabelle mit 0 (null) Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="002fe-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="002fe-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="002fe-120">MFCMAPI reference</span></span>

<span data-ttu-id="002fe-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="002fe-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="002fe-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="002fe-122">**File**</span></span>|<span data-ttu-id="002fe-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="002fe-123">**Function**</span></span>|<span data-ttu-id="002fe-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="002fe-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="002fe-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="002fe-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="002fe-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="002fe-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="002fe-127">MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::GetMsgServiceTable** -Methode zum Laden der Tabelle der Dienste in einem Profil in der Ansicht gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="002fe-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="002fe-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="002fe-128">See also</span></span>



[<span data-ttu-id="002fe-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="002fe-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="002fe-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="002fe-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="002fe-131">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="002fe-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="002fe-132">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="002fe-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

