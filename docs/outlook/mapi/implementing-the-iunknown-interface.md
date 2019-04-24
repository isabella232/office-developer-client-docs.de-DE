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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310045"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="d7729-103">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d7729-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="d7729-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7729-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7729-105">Die Methoden der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle, die in jedem MAPI-Objekt implementiert sind, unterstützen die Kommunikation zwischen Objekten und die Objektverwaltung.</span><span class="sxs-lookup"><span data-stu-id="d7729-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="d7729-106">**IUnknown** verfügt über drei Methoden: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)und [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7729-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="d7729-107">**QueryInterface** ermöglicht es einem Objekt, zu bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d7729-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="d7729-108">Mit **QueryInterface**können zwei Objekte, die keine Vorkenntnisse der Funktionalität des jeweils anderen besitzen, interagieren.</span><span class="sxs-lookup"><span data-stu-id="d7729-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="d7729-109">Wenn das Objekt, das **QueryInterface** implementiert, die fragliche Schnittstelle unterstützt, wird ein Zeiger auf die Implementierung der Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7729-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="d7729-110">Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, wird der MAPI_E_INTERFACE_NOT_SUPPORTED-Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7729-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="d7729-111">Wenn **QueryInterface** einen angeforderten Schnittstellenzeiger zurückgibt, muss auch der Verweiszähler des neuen Objekts erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="d7729-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="d7729-112">Der Verweiszähler eines Objekts ist ein numerischer Wert, der zum Verwalten der Lebensdauer des Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7729-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="d7729-113">Wenn der Verweiszähler größer als 1 ist, kann der Arbeitsspeicher des Objekts nicht freigegeben werden, da er aktiv verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7729-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="d7729-114">Nur wenn der Verweiszähler auf 0 sinkt, kann das Objekt sicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7729-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="d7729-115">Die anderen beiden **IUnknown** -Methoden **AddRef** und **Release**verwalten den Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="d7729-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="d7729-116">**AddRef** inkrementiert den Verweiszähler, während die **Freigabe** ihn dekrementiert.</span><span class="sxs-lookup"><span data-stu-id="d7729-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="d7729-117">Alle Methoden oder API-Funktionen, die Schnittstellenzeiger wie **QueryInterface**zurückgeben, müssen **AddRef** aufrufen, um den Verweiszähler zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d7729-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="d7729-118">Alle Implementierungen von Methoden, die Schnittstellenzeiger empfangen, müssen die **Freigabe** aufrufen, um die Anzahl zu verringern, wenn der Zeiger nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7729-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="d7729-119">**Release** prüft einen vorhandenen Verweiszähler, der den der Schnittstelle zugeordneten Arbeitsspeicher nur freigibt, wenn die Anzahl 0 ist.</span><span class="sxs-lookup"><span data-stu-id="d7729-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7729-120">Da **AddRef** und **Release** keine genauen Werte zurückgeben müssen, dürfen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um zu bestimmen, ob ein Objekt noch gültig ist oder zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="d7729-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7729-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7729-121">See also</span></span>



[<span data-ttu-id="d7729-122">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="d7729-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

