---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792305"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="c9194-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="c9194-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="c9194-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9194-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9194-105">MAPI-Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="c9194-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="c9194-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9194-106">Parameters</span></span>

 <span data-ttu-id="c9194-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c9194-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c9194-108">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9194-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="c9194-109">Dieser Parameter wird ignoriert, wenn das Flag MAPI_LOGOFF_UI nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c9194-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="c9194-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9194-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c9194-111">[in] Eine Bitmaske aus Flags, die den Vorgang zum Abmelden steuern.</span><span class="sxs-lookup"><span data-stu-id="c9194-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="c9194-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c9194-112">The following flags can be set:</span></span>
    
<span data-ttu-id="c9194-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="c9194-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="c9194-114">Wenn dieser Sitzung freigegeben ist, sollte die Abmeldung alle Clients, die mithilfe der freigegebenen Sitzung angemeldeten benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c9194-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="c9194-115">Die Clients sollten melden Sie sich ab.</span><span class="sxs-lookup"><span data-stu-id="c9194-115">The clients should log off.</span></span> <span data-ttu-id="c9194-116">Jeder Client, der die freigegebene Sitzung verwendet wird, kann dieses Kennzeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9194-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="c9194-117">MAPI_LOGOFF_SHARED wird ignoriert, wenn die aktuelle Sitzung nicht freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c9194-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="c9194-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="c9194-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="c9194-119">**Abmelden** können während des Vorgangs ein Dialogfeld anzeigen möglicherweise der Benutzer zur Bestätigung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c9194-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="c9194-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="c9194-120">_ulReserved_</span></span>
  
> <span data-ttu-id="c9194-121">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="c9194-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9194-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9194-122">Return value</span></span>

<span data-ttu-id="c9194-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9194-123">S_OK</span></span> 
  
> <span data-ttu-id="c9194-124">Der Vorgang zum Abmelden war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c9194-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9194-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9194-125">Remarks</span></span>

<span data-ttu-id="c9194-126">Die **IMAPISession::Logoff** -Methode wird eine MAPI-Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="c9194-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="c9194-127">Wenn **Abmelden** zurückgegeben wird, kann keine der Methoden außer [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c9194-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9194-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c9194-128">Notes to callers</span></span>

<span data-ttu-id="c9194-129">Wenn **Abmelden** zurückgibt, release Session-Objekt durch die **IUnknown** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9194-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="c9194-130">Weitere Informationen zum Beenden einer Sitzung finden Sie unter [Beenden einer MAPI-Sitzung](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="c9194-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9194-131">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c9194-131">MFCMAPI reference</span></span>

<span data-ttu-id="c9194-132">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c9194-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9194-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c9194-133">**File**</span></span>|<span data-ttu-id="c9194-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c9194-134">**Function**</span></span>|<span data-ttu-id="c9194-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c9194-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9194-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="c9194-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="c9194-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="c9194-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="c9194-138">MFCMAPI (engl.) verwendet die **IMAPISession::Logoff** -Methode aus der Sitzung vor einer Freigabe abmelden.</span><span class="sxs-lookup"><span data-stu-id="c9194-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c9194-139">Aufgrund der Verhalten für Schnelles Herunterfahren in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 und Microsoft Outlook 2013 eingeführt sollten Clients nie Parameters **MAPI_LOGOFF_SHARED** [IMAPISession::Logoff](imapisession-logoff.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="c9194-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="c9194-140">Übergeben von **MAPI_LOGOFF_SHARED** bewirkt, dass alle MAPI-Clients zum Herunterfahren beginnen und unerwartetes Verhalten tritt.</span><span class="sxs-lookup"><span data-stu-id="c9194-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9194-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9194-141">See also</span></span>



[<span data-ttu-id="c9194-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9194-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="c9194-143">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c9194-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c9194-144">Beenden einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="c9194-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

