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
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309625"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="81720-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="81720-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="81720-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81720-105">Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="81720-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="81720-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81720-106">Parameters</span></span>

 <span data-ttu-id="81720-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="81720-107">_lpClassID_</span></span>
  
> <span data-ttu-id="81720-108">[in, out] Ein Zeiger auf die Klassen-ID (CLSID) des Formulars.</span><span class="sxs-lookup"><span data-stu-id="81720-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81720-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81720-109">Return value</span></span>

<span data-ttu-id="81720-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="81720-110">S_OK</span></span> 
  
> <span data-ttu-id="81720-111">Der Klassenbezeichner wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81720-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81720-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81720-112">Remarks</span></span>

<span data-ttu-id="81720-113">Mit der **IPersistMessge:: GetClassID** -Methode werden die Inhalte des _lpClassID_ -Parameters auf den Klassenbezeichner des Formular Servers festgelegt und S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81720-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="81720-114">Wenn ein Formular Betrachter **GetClassID** aufruft und erfolgreich zurückgegeben wird, wird das Formular in den Zustand "nicht [Initialisiert](uninitialized-state.md) " versetzt.</span><span class="sxs-lookup"><span data-stu-id="81720-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="81720-115">Weitere Informationen dazu, wie Klassenbezeichner mit strukturierten Speicherobjekten verwendet werden, finden Sie in der Dokumentation zur [IPersist:: GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="81720-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81720-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81720-116">See also</span></span>



[<span data-ttu-id="81720-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81720-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

