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
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="3d6fe-103">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3d6fe-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="3d6fe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d6fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d6fe-105">Die Methoden der [IUnknown-Schnittstelle,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) die in jedem MAPI-Objekt implementiert sind, unterstützen die Kommunikation zwischen Objekten und die Objektverwaltung.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="3d6fe-106">**IUnknown** hat drei Methoden: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)und [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3d6fe-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="3d6fe-107">**Mit QueryInterface** kann ein Objekt bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="3d6fe-108">Mit **QueryInterface** können zwei Objekte interagieren, die sich nicht über die Funktionalität der anderen benutzerintern im Voraus kennen.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="3d6fe-109">Wenn das Objekt, das **QueryInterface** implementiert, die in Frage gestellte Schnittstelle unterstützt, gibt es einen Zeiger auf die Implementierung der Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="3d6fe-110">Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, gibt es den wert MAPI_E_INTERFACE_NOT_SUPPORTED zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="3d6fe-111">Wenn **QueryInterface** einen angeforderten Schnittstellenzeiger zurückgibt, muss auch die Referenzanzahl des neuen Objekts erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="3d6fe-112">Die Referenzanzahl eines Objekts ist ein numerischer Wert, der zum Verwalten der Lebensdauer des Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="3d6fe-113">Wenn die Referenzanzahl größer als 1 ist, kann der Arbeitsspeicher des Objekts nicht frei werden, da es aktiv verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="3d6fe-114">Nur wenn die Referenzanzahl auf 0 fällt, kann das Objekt sicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="3d6fe-115">Die beiden anderen **IUnknown-Methoden** **AddRef** und **Release** verwalten die Referenzanzahl.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="3d6fe-116">**AddRef** erhöht die Referenzanzahl, während **Release** sie dekrementiert.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="3d6fe-117">Alle Methoden oder API-Funktionen, die Schnittstellenzeiger zurückgeben, z. B. **QueryInterface**, müssen **AddRef aufrufen,** um die Referenzanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="3d6fe-118">Alle Implementierungen von Methoden, die Schnittstellenzeiger empfangen, müssen **Release** aufrufen, um die Anzahl zu dekrementieren, wenn der Zeiger nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="3d6fe-119">**Die** Freigabe überprüft auf eine vorhandene Referenzanzahl und gibt den der Schnittstelle zugeordneten Arbeitsspeicher nur frei, wenn die Anzahl 0 ist.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3d6fe-120">Da **AddRef** und **Release** keine genauen Werte zurückgeben müssen, dürfen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um zu ermitteln, ob ein Objekt noch gültig ist oder zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="3d6fe-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d6fe-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d6fe-121">See also</span></span>



[<span data-ttu-id="3d6fe-122">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="3d6fe-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

