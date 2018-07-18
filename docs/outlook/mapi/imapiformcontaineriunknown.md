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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792154"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="8c7d1-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c7d1-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="8c7d1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c7d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c7d1-105">Formulare in Formularbibliotheken verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-105">Manages forms in form libraries.</span></span> <span data-ttu-id="8c7d1-106">Diese Schnittstelle wird verwendet, um anwendungsspezifische Formularbibliotheken erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c7d1-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8c7d1-107">Header file:</span></span>  <br/> |<span data-ttu-id="8c7d1-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="8c7d1-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8c7d1-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="8c7d1-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8c7d1-110">Formular Container-Objekte</span><span class="sxs-lookup"><span data-stu-id="8c7d1-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="8c7d1-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8c7d1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c7d1-112">Anbieter für Formular-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c7d1-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="8c7d1-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8c7d1-113">Called by:</span></span>  <br/> |<span data-ttu-id="8c7d1-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="8c7d1-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="8c7d1-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8c7d1-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8c7d1-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="8c7d1-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="8c7d1-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="8c7d1-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8c7d1-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="8c7d1-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8c7d1-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8c7d1-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8c7d1-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="8c7d1-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="8c7d1-121">Installiert ein Formular in einem Formular-Container.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="8c7d1-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="8c7d1-123">Entfernt ein bestimmtes Formular aus einem Formular Container.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="8c7d1-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="8c7d1-125">Löst eine Nachrichtenklasse in seiner Form in einem Formular Container und ein Formular Informationen-Objekt für dieses Formular zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="8c7d1-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="8c7d1-127">Eine Gruppe von Nachrichtenklassen in Formularen in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="8c7d1-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="8c7d1-129">Gibt ein Array der Eigenschaften verwendet, die für alle Formen in einem Formular Container installiert.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="8c7d1-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="8c7d1-131">Gibt den Anzeigenamen eines Containers Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="8c7d1-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="8c7d1-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="8c7d1-133">Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler auftritt, auf das Formular Container-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8c7d1-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c7d1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c7d1-134">See also</span></span>



[<span data-ttu-id="8c7d1-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8c7d1-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

