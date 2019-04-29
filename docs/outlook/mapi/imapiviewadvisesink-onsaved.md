---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407606"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="47437-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="47437-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="47437-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47437-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47437-105">Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht in einem Formular gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="47437-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="47437-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47437-106">Parameters</span></span>

<span data-ttu-id="47437-107">Keine</span><span class="sxs-lookup"><span data-stu-id="47437-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="47437-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47437-108">Return value</span></span>

<span data-ttu-id="47437-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="47437-109">S_OK</span></span> 
  
> <span data-ttu-id="47437-110">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="47437-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47437-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47437-111">Remarks</span></span>

<span data-ttu-id="47437-112">Ein Form-Objekt ruft die **IMAPIViewAdviseSink::** onsaved-Methode auf, nachdem die aktuelle Nachricht in einem Formular erfolgreich gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="47437-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="47437-113">Auf diese Weise können die Betrachter Ihre Fenster aktualisieren, um Änderungen an der Nachricht widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="47437-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="47437-114">Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="47437-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47437-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47437-115">See also</span></span>



[<span data-ttu-id="47437-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47437-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

