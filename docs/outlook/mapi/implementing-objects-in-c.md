---
title: Implementieren von Objekten in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414942"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="c1ff4-103">Implementieren von Objekten in C</span><span class="sxs-lookup"><span data-stu-id="c1ff4-103">Implementing objects in C</span></span>

<span data-ttu-id="c1ff4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1ff4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1ff4-105">In C geschriebene Clientanwendungen und Dienstanbieter definieren #A0 durch Erstellen einer Datenstruktur und eines Arrays von geordneten Funktionszeigern, die als virtuelle Funktionstabelle oder vtable bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="c1ff4-106">Ein Zeiger auf die vtable muss das erste Element der Datenstruktur sein.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="c1ff4-107">In der vtable selbst gibt es einen Zeiger für jede Methode in jeder Schnittstelle, die vom Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="c1ff4-108">Die Reihenfolge der Zeiger muss der Reihenfolge der Methoden in der In der Mapidefs.h-Headerdatei veröffentlichten Schnittstellenspezifikation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="c1ff4-109">Jeder Funktionszeiger in der vtable wird auf die Adresse der tatsächlichen Implementierung der Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="c1ff4-110">In C++ richtet der Compiler die vtable automatisch ein.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="c1ff4-111">In C nicht.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-111">In C, it does not.</span></span> 
  
<span data-ttu-id="c1ff4-112">Die folgende Abbildung zeigt, wie dies funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-112">The following illustration shows how this works.</span></span> <span data-ttu-id="c1ff4-113">Das Feld ganz links stellt einen Client dar, der ein Dienstanbieterobjekt verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="c1ff4-114">Über die Sitzung ruft der Client einen Zeiger auf das Objekt, **lpObject , ab.**</span><span class="sxs-lookup"><span data-stu-id="c1ff4-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="c1ff4-115">Die vtable wird zuerst im Objekt angezeigt, gefolgt von privaten Daten und Methoden.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="c1ff4-116">Der vtable-Zeiger zeigt auf die tatsächliche vtable, die Zeiger auf jede Implementierung der Methoden in der Schnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="c1ff4-117">**Objektimplementierung**</span><span class="sxs-lookup"><span data-stu-id="c1ff4-117">**Object implementation**</span></span>
  
<span data-ttu-id="c1ff4-118">![Objektimplementierung](media/amapi_42.gif "Objektimplementierung")</span><span class="sxs-lookup"><span data-stu-id="c1ff4-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="c1ff4-119">Das folgende Codebeispiel zeigt, wie ein C-Dienstanbieter ein einfaches Statusobjekt definieren kann.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="c1ff4-120">Das erste Element ist der #A0 Der Rest des Objekts besteht aus Datenm membern.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

<span data-ttu-id="c1ff4-121">Da es sich bei diesem Objekt um ein Statusobjekt handelt, enthält die vtable Zeiger auf Implementierungen der einzelnen Methoden in der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) sowie Zeiger auf Implementierungen der einzelnen Methoden in den Basisschnittstellen – **IUnknown** und **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="c1ff4-122">Die Reihenfolge der Methoden in der vtable entspricht der angegebenen Reihenfolge, die in der Mapidefs.h-Headerdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

<span data-ttu-id="c1ff4-123">In C geschriebene Clients und Dienstanbieter verwenden Objekte indirekt über die vtable und fügen einen Objektzeiger als ersten Parameter in jedem Aufruf hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="c1ff4-124">Jeder Aufruf einer MAPI-Schnittstellenmethode erfordert einen Zeiger auf das Objekt, das als erster Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="c1ff4-125">C++ definiert einen speziellen Zeiger, der zu diesem Zweck als **dieser** Zeiger bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="c1ff4-126">Der C++-Compiler fügt  den Zeiger implizit als ersten Parameter zu jedem Methodenaufruf hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="c1ff4-127">In C gibt es keinen solchen Zeiger. sie muss explizit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c1ff4-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="c1ff4-128">Der folgende Code veranschaulicht, wie ein Client eine Instanz von MYSTATUSOBJECT aufrufen kann:</span><span class="sxs-lookup"><span data-stu-id="c1ff4-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="c1ff4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1ff4-129">See also</span></span>

- [<span data-ttu-id="c1ff4-130">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="c1ff4-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

