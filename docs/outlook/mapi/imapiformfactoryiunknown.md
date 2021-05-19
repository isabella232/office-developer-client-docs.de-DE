---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342119"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="2aa09-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aa09-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="2aa09-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aa09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aa09-105">Unterstützt die Verwendung konfigurierbarer Laufzeitformulare in verteilten Computerumgebungen.</span><span class="sxs-lookup"><span data-stu-id="2aa09-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aa09-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2aa09-106">Header file:</span></span>  <br/> |<span data-ttu-id="2aa09-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="2aa09-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2aa09-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="2aa09-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2aa09-109">Form Factory-Objekte</span><span class="sxs-lookup"><span data-stu-id="2aa09-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="2aa09-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2aa09-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2aa09-111">Formularserver</span><span class="sxs-lookup"><span data-stu-id="2aa09-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="2aa09-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2aa09-112">Called by:</span></span>  <br/> |<span data-ttu-id="2aa09-113">Formularanzeigen</span><span class="sxs-lookup"><span data-stu-id="2aa09-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="2aa09-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2aa09-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2aa09-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="2aa09-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="2aa09-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="2aa09-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2aa09-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="2aa09-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2aa09-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2aa09-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2aa09-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="2aa09-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="2aa09-120">Gibt ein Klassen factory-Objekt für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="2aa09-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="2aa09-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2aa09-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="2aa09-122">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2aa09-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="2aa09-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="2aa09-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="2aa09-124">Behält einen geöffneten Formularserver im Arbeitsspeicher bei.</span><span class="sxs-lookup"><span data-stu-id="2aa09-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aa09-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2aa09-125">Remarks</span></span>

<span data-ttu-id="2aa09-126">Die **IMAPIFormFactory-Schnittstelle** basiert auf der [IClassFactory-Schnittstelle,](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) und Objekte, die **IMAPIFormFactory** implementieren, sollten auch von **IClassFactory erben.**</span><span class="sxs-lookup"><span data-stu-id="2aa09-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="2aa09-127">**IMAPIFormFactory** ist die Schnittstelle, mit der Formularanzeigen neue Formularobjekte erstellen, wenn ein Formularserver mehrere Nachrichtenklassen unterstützt (d. h. mehr als einen Formularobjekttyp).</span><span class="sxs-lookup"><span data-stu-id="2aa09-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2aa09-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aa09-128">See also</span></span>



[<span data-ttu-id="2aa09-129">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2aa09-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

