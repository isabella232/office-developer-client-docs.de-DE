---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c9d769e6a32fad22750a965debbbdce83e4de539
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586458"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="9ffe8-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="9ffe8-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="9ffe8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ffe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ffe8-105">Gibt einen Bezeichner, der den Formular Server darstellt, der das Formular verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="9ffe8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ffe8-106">Parameters</span></span>

 <span data-ttu-id="9ffe8-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="9ffe8-107">_lpClassID_</span></span>
  
> <span data-ttu-id="9ffe8-108">[in, out] Ein Zeiger auf die Klassen-ID (CLSID) des Formulars.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ffe8-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9ffe8-109">Return value</span></span>

<span data-ttu-id="9ffe8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ffe8-110">S_OK</span></span> 
  
> <span data-ttu-id="9ffe8-111">Die Klassen-ID wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ffe8-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9ffe8-112">Remarks</span></span>

<span data-ttu-id="9ffe8-113">Die **IPersistMessge::GetClassID** -Methode wird die Inhalte des Parameters _LpClassID_ auf dem Formular Server Klassen-ID und gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="9ffe8-114">Wenn ein Formular Viewer **GetClassID** aufruft und erfolgreich zurückgegeben, wird das Formular in den Status [nicht initialisiert](uninitialized-state.md) platziert.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="9ffe8-115">Weitere Informationen darüber, wie Klassenbezeichner mit strukturierten Speicherobjekte verwendet werden finden Sie unter der Dokumentation für die [IPersist:: GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9ffe8-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ffe8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ffe8-116">See also</span></span>



[<span data-ttu-id="9ffe8-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ffe8-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

