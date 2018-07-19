---
title: Implementieren von Objekten in C#
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 71a8dc6472051e72d990a5c5d6f026ae63f1df25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792570"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="2096f-103">Implementieren von Objekten in C#</span><span class="sxs-lookup"><span data-stu-id="2096f-103">Implementing objects in C</span></span>

<span data-ttu-id="2096f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2096f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2096f-105">Clientanwendungen und Dienstanbieter in C# geschriebenen definieren MAPI-Objekten, indem Sie erstellen eine Datenstruktur und ein Array von geordnete Funktionszeiger als virtuelle Funktion Tabellen oder Vtable bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2096f-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="2096f-106">Ein Zeiger auf die Vtable muss das erste Element der Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="2096f-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="2096f-107">In der Vtable selbst wird einen Zeiger für jede Methode in jede Schnittstelle, die durch das Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2096f-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="2096f-108">Die Reihenfolge der Zeiger muss die Reihenfolge der Methoden in der Schnittstellenspezifikation veröffentlicht in der Headerdatei Mapidefs.h folgen.</span><span class="sxs-lookup"><span data-stu-id="2096f-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="2096f-109">Jeder Funktionszeiger in der Vtable wird auf die Adresse der tatsächlichen Implementierung der-Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2096f-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="2096f-110">In C++ richtet der Compiler automatisch die Vtable.</span><span class="sxs-lookup"><span data-stu-id="2096f-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="2096f-111">In C ist es nicht.</span><span class="sxs-lookup"><span data-stu-id="2096f-111">In C, it does not.</span></span> 
  
<span data-ttu-id="2096f-112">Die folgende Abbildung zeigt, wie dies funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2096f-112">The following illustration shows how this works.</span></span> <span data-ttu-id="2096f-113">Das Feld ganz links stellt einen Client, der eine dienstanbieterobjekts verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="2096f-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="2096f-114">In der Sitzung erhält der Client einen Zeiger auf das **LpObject**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2096f-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="2096f-115">Die Vtable wird zuerst in das Objekt gefolgt von privaten Daten und Methoden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2096f-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="2096f-116">Der Vtable-Zeiger verweist auf die tatsächliche Vtable, die Zeiger auf die einzelnen Implementierungen der Methoden in der Benutzeroberfläche der enthält.</span><span class="sxs-lookup"><span data-stu-id="2096f-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="2096f-117">**Objektimplementierung**</span><span class="sxs-lookup"><span data-stu-id="2096f-117">**Object implementation**</span></span>
  
<span data-ttu-id="2096f-118">![Objektimplementierung] (media/amapi_42.gif "Objektimplementierung")</span><span class="sxs-lookup"><span data-stu-id="2096f-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="2096f-119">Das folgende Codebeispiel zeigt, wie ein C#-Dienstanbieter ein einfaches Statusobjekt definieren kann.</span><span class="sxs-lookup"><span data-stu-id="2096f-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="2096f-120">Das erste Element ist der Vtable-Zeiger; der Rest des Objekts Datenmember besteht.</span><span class="sxs-lookup"><span data-stu-id="2096f-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
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

<span data-ttu-id="2096f-121">Da dieses Objekt ein Statusobjekt ist, enthält die Vtable Zeigern für Implementierungen der einzelnen Methoden in der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle sowie Zeiger auf Implementierungen der einzelnen Methoden in die Basis Schnittstellen – **IUnknown **und **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="2096f-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="2096f-122">Die Reihenfolge der Methoden in der Vtable entspricht die angegebene Reihenfolge in der Headerdatei Mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="2096f-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
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

<span data-ttu-id="2096f-123">Clients-Dienstanbieter in C# geschriebenen Objekte indirekt über Vtable und verwenden einen Zeiger als der erste Parameter in jedem Aufruf hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2096f-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="2096f-124">Alle Anrufe an einen MAPI-Schnittstelle-Methode erfordert einen Zeiger auf das Objekt als erster Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2096f-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="2096f-125">C++ definiert einen speziellen Mauszeiger bekannt als **this** -Zeiger für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="2096f-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="2096f-126">Der C++ Compiler hinzugefügt **this** -Zeiger implizit als der erste Parameter auf jedem Methodenaufruf.</span><span class="sxs-lookup"><span data-stu-id="2096f-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="2096f-127">In C# ist keine solche Zeiger; Es muss explizit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2096f-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="2096f-128">Im folgenden Code wird veranschaulicht, wie ein Client einen Anruf mit einer Instanz des MYSTATUSOBJECT tätigen kann:</span><span class="sxs-lookup"><span data-stu-id="2096f-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="2096f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2096f-129">See also</span></span>

- [<span data-ttu-id="2096f-130">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="2096f-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

