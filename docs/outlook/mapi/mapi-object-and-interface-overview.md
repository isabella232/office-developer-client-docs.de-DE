---
title: MAPI-Objekt und Übersicht über die Benutzeroberfläche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8882457ff99f4150f2c9b086b92af32de29d60a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793018"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="3141d-103">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3141d-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="3141d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3141d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3141d-105">Ein MAPI-Objekt ist eine C++-Objektklassen oder C-Datenstruktur, die von einer oder mehreren MAPI-Schnittstellen oder Sammlungen verwandter Funktionen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="3141d-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="3141d-106">Diese Sammlungen verwandter Funktionen werden als reinen virtuellen Funktionen für C++-Entwickler bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3141d-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="3141d-107">Bei einer reinen virtuellen Funktion liefert MAPI nur Funktionsprototyp keine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3141d-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="3141d-108">Es wird erwartet, dass eine Clientanwendung, einem Dienstanbieter oder MAPI dieser Implementierung leistet durch Erstellen einer Objektklassen, die von der Schnittstelle erbt und die Funktion Beschreibungen der Messaging-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="3141d-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="3141d-109">Eine MAPI-Schnittstelle kann nur über eine geerbte Klasse instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="3141d-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="3141d-110">Es gibt viele verschiedene MAPI-Objekte, jedes Objekt erben von eine Schnittstelle, die letztlich vom die [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) -Schnittstelle geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="3141d-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="3141d-111">**IUnknown** ist die Basis OLE Component Object Model (COM)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3141d-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="3141d-112">Softwareentwicklern MAPI-Objekte mit einem standard Mechanismus für die Kommunikation und Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3141d-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="3141d-113">COM bestimmt Behandlung Objekt Implementierer Probleme wie Arbeitsspeicher Parameter Management, Verwaltung und multithreading.</span><span class="sxs-lookup"><span data-stu-id="3141d-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="3141d-114">Durch dieses Modell angleichen, wird ein Objekt Implementierer einen Vertrag gemäß von den Schnittstellen im Objekt eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3141d-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="3141d-115">Viele MAPI-Schnittstellen geerbt werden direkt von **IUnknown**, während andere indirekt über eine der beiden anderen Basiskalender Schnittstellen vererbt werden: [IMAPIProp: IUnknown](imapipropiunknown.md) für die Eigenschaft Verwaltung und [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) für Ordner und Address Book Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3141d-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="3141d-116">Base-Schnittstellen werden nie als separate, eigenständige Objekte implementiert. Sie werden immer als Teil des anderen Objekten implementiert, abgeleitete Objekte, mit denen implementiert Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3141d-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="3141d-117">MAPI definiert viele andere Arten von Objekten, die jeweils durch eine oder mehrere MAPI-Komponenten implementiert.</span><span class="sxs-lookup"><span data-stu-id="3141d-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="3141d-118">Objekte, die von Clients implementiert werden von MAPI, Dienstanbieter und benutzerdefinierte Formularkomponenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3141d-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="3141d-119">Objekte, die vom Dienstanbieter implementiert werden in der Regel durch MAPI- und -Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="3141d-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="3141d-120">Objekte von Formular Bibliothek Anbietern implementiert und Formular Servern werden von anderen Formularkomponenten und -Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="3141d-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3141d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3141d-121">See also</span></span>



[<span data-ttu-id="3141d-122">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3141d-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="3141d-123">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3141d-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="3141d-124">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="3141d-124">MAPI Concepts</span></span>](mapi-concepts.md)

