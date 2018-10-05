---
title: Implementieren der IUnknown-Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397415"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="043f3-103">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="043f3-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="043f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="043f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="043f3-105">Die Methoden für die [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle implementiert, die in jedem MAPI-Objekt unterstützt interobject Kommunikation und Objekt Management.</span><span class="sxs-lookup"><span data-stu-id="043f3-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="043f3-106">**IUnknown** verfügt über drei Methoden: [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)und [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="043f3-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="043f3-107">**QueryInterface** ermöglicht, ein Objekt zu bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="043f3-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="043f3-108">Mit **QueryInterface**können ohne vorherige Kenntnisse der Funktionalität des jeweils anderen zwei Objekte interagieren.</span><span class="sxs-lookup"><span data-stu-id="043f3-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="043f3-109">Wenn das Objekt, **das QueryInterface** implementiert, die betreffende-Schnittstelle unterstützt, gibt es einen Zeiger auf die Implementierung der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="043f3-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="043f3-110">Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, wird den Wert MAPI_E_INTERFACE_NOT_SUPPORTED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="043f3-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="043f3-111">Wenn **QueryInterface** einen Zeiger angeforderte Schnittstelle zurückgegeben wird, muss auch das neue Objekt Referenzzähler erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="043f3-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="043f3-112">Ein Objekt Referenzzähler ist einen numerischen Wert verwendet, um das Objekt Lebensdauer verwalten.</span><span class="sxs-lookup"><span data-stu-id="043f3-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="043f3-113">Bei der Referenzzähler größer als 1 ist, wird der Speicher des Objekts kann nicht freigegeben werden, da sie aktiv verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="043f3-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="043f3-114">Es ist nur bei der Referenzzähler 0 erreicht, dass das Objekt sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="043f3-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="043f3-115">Die anderen beiden **IUnknown** -Methoden, **AddRef** und **Release**, verwalten den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="043f3-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="043f3-116">**AddRef** erhöht den Referenzzähler, während der **Freigabe** dekrementiert es.</span><span class="sxs-lookup"><span data-stu-id="043f3-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="043f3-117">Alle Methoden oder API-Funktionen, die Schnittstellenzeiger, wie etwa **QueryInterface**, zurückgeben müssen **AddRef** um erhöht den Referenzzähler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="043f3-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="043f3-118">Alle Implementierungen der Methoden, die Schnittstellenzeiger erhalten müssen aufrufen, **Version** , um die Anzahl der zu verringern, wenn der Mauszeiger nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="043f3-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="043f3-119">**Version** überprüft einer vorhandenen Referenzzähler den Speicher nur, wenn die Anzahl 0 ist die Schnittstelle zugeordnete freigibt.</span><span class="sxs-lookup"><span data-stu-id="043f3-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="043f3-120">Da **AddRef** und **Release** nicht erforderlich, genaue Werte zurückgeben, müssen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um festzustellen, ob ein Objekt noch gültig ist, oder gelöscht wurde wurde.</span><span class="sxs-lookup"><span data-stu-id="043f3-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="043f3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="043f3-121">See also</span></span>



[<span data-ttu-id="043f3-122">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="043f3-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

