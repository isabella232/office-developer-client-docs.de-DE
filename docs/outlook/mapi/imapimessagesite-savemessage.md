---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ec85f7bdfc9d2d275bdb5ffe7ba0113ad4a35c3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792228"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="25b10-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="25b10-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="25b10-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25b10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25b10-105">Anforderungen, die die aktuelle Nachricht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25b10-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="25b10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b10-106">Parameters</span></span>

<span data-ttu-id="25b10-107">None.</span><span class="sxs-lookup"><span data-stu-id="25b10-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="25b10-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="25b10-108">Return value</span></span>

<span data-ttu-id="25b10-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="25b10-109">S_OK</span></span> 
  
> <span data-ttu-id="25b10-110">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="25b10-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="25b10-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25b10-111">Remarks</span></span>

<span data-ttu-id="25b10-112">Formulare rufen Sie die **IMAPIMessageSite::SaveMessage** -Methode, um anzufordern, dass eine Nachricht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="25b10-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="25b10-113">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="25b10-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="25b10-114">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="25b10-114">MFCMAPI reference</span></span>

<span data-ttu-id="25b10-115">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="25b10-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="25b10-116">**Datei**</span><span class="sxs-lookup"><span data-stu-id="25b10-116">**File**</span></span>|<span data-ttu-id="25b10-117">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="25b10-117">**Function**</span></span>|<span data-ttu-id="25b10-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="25b10-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25b10-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="25b10-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="25b10-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="25b10-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="25b10-121">MFCMAPI (engl.) verwendet die **IMAPIMessageSite::SaveMessage** -Methode, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="25b10-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25b10-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25b10-122">See also</span></span>



[<span data-ttu-id="25b10-123">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="25b10-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="25b10-124">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="25b10-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="25b10-125">MAPI-Formulars Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="25b10-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

