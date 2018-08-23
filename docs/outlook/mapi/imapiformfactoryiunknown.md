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
ms.openlocfilehash: b2aa08ea14df87f24cda3da0137ae4bfa2c50b40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576015"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="51c63-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51c63-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="51c63-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c63-105">Unterstützt die Verwendung von konfigurierbar Laufzeit-Formularen in einer verteilten Umgebung Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="51c63-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51c63-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="51c63-106">Header file:</span></span>  <br/> |<span data-ttu-id="51c63-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="51c63-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="51c63-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="51c63-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="51c63-109">Formular Factory-Objekte</span><span class="sxs-lookup"><span data-stu-id="51c63-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="51c63-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="51c63-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="51c63-111">Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="51c63-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="51c63-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="51c63-112">Called by:</span></span>  <br/> |<span data-ttu-id="51c63-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="51c63-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="51c63-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="51c63-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="51c63-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="51c63-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="51c63-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="51c63-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="51c63-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="51c63-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="51c63-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="51c63-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="51c63-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="51c63-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="51c63-120">Gibt ein Klasse Factory-Objekt für das Formular.</span><span class="sxs-lookup"><span data-stu-id="51c63-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="51c63-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="51c63-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="51c63-122">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, auf das Formular Factory-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="51c63-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="51c63-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="51c63-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="51c63-124">Wird einen geöffnete Formular Server im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="51c63-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c63-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="51c63-125">Remarks</span></span>

<span data-ttu-id="51c63-126">Die Schnittstelle **IMAPIFormFactory** basiert auf der [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) -Schnittstelle und Objekte, die **IMAPIFormFactory** implementieren sollten auch von **IClassFactory**erben.</span><span class="sxs-lookup"><span data-stu-id="51c63-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="51c63-127">**IMAPIFormFactory** ist die Schnittstelle, die Formular Viewer verwenden, um die neue Formularobjekte zu erstellen, wenn ein Formular Server mehr als eine Nachrichtenklasse unterstützt (d. h., mehrere Typ der Form-Objekt).</span><span class="sxs-lookup"><span data-stu-id="51c63-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51c63-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51c63-128">See also</span></span>



[<span data-ttu-id="51c63-129">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="51c63-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

