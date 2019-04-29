---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407529"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="8e1a3-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e1a3-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="8e1a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e1a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e1a3-105">Verwaltet Formulare in Formularbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-105">Manages forms in form libraries.</span></span> <span data-ttu-id="8e1a3-106">Diese Schnittstelle wird verwendet, um anwendungsspezifische Formularbibliotheken zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e1a3-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8e1a3-107">Header file:</span></span>  <br/> |<span data-ttu-id="8e1a3-108">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="8e1a3-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8e1a3-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="8e1a3-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8e1a3-110">Formular Containerobjekte</span><span class="sxs-lookup"><span data-stu-id="8e1a3-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="8e1a3-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8e1a3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e1a3-112">Formular Bibliotheks Anbieter</span><span class="sxs-lookup"><span data-stu-id="8e1a3-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="8e1a3-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8e1a3-113">Called by:</span></span>  <br/> |<span data-ttu-id="8e1a3-114">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8e1a3-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="8e1a3-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8e1a3-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8e1a3-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="8e1a3-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="8e1a3-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="8e1a3-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8e1a3-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="8e1a3-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8e1a3-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8e1a3-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8e1a3-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="8e1a3-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="8e1a3-121">Installiert ein Formular in einem Formular Container.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="8e1a3-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="8e1a3-123">Entfernt ein bestimmtes Formular aus einem Formular Container.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="8e1a3-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="8e1a3-125">Löst eine Nachrichtenklasse in Ihrem Formular in einem Formular Container auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="8e1a3-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="8e1a3-127">Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare in einem Formular Container auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="8e1a3-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="8e1a3-129">Gibt ein Array der Eigenschaften zurück, die von allen in einem Formular Container installierten Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="8e1a3-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="8e1a3-131">Gibt den Anzeigenamen eines Formular Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="8e1a3-132">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="8e1a3-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="8e1a3-133">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen über den vorherigen Fehler im Formular Containerobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="8e1a3-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e1a3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e1a3-134">See also</span></span>



[<span data-ttu-id="8e1a3-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e1a3-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

