---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414004"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="e5581-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="e5581-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="e5581-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5581-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5581-105">Gibt einen Zeiger auf den Formularcontainer zurück, in dem ein bestimmtes Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5581-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="e5581-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5581-106">Parameters</span></span>

 <span data-ttu-id="e5581-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="e5581-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="e5581-108">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularcontainerobjekt.</span><span class="sxs-lookup"><span data-stu-id="e5581-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5581-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5581-109">Return value</span></span>

<span data-ttu-id="e5581-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5581-110">S_OK</span></span> 
  
> <span data-ttu-id="e5581-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e5581-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5581-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5581-112">See also</span></span>



[<span data-ttu-id="e5581-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e5581-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

