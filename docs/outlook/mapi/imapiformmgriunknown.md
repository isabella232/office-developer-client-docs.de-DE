---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792197"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="c1e23-103">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1e23-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="c1e23-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1e23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1e23-105">Ermöglicht das Formular Zuschauer zu Informationen zum Beziehen und Aktivieren von Formular Servern.</span><span class="sxs-lookup"><span data-stu-id="c1e23-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1e23-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c1e23-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1e23-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c1e23-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c1e23-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="c1e23-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c1e23-109">Formular-Manager-Objekte</span><span class="sxs-lookup"><span data-stu-id="c1e23-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="c1e23-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c1e23-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1e23-111">Anbieter für Formular-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1e23-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="c1e23-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c1e23-112">Called by:</span></span>  <br/> |<span data-ttu-id="c1e23-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="c1e23-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="c1e23-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c1e23-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c1e23-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="c1e23-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="c1e23-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="c1e23-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c1e23-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="c1e23-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c1e23-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c1e23-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c1e23-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="c1e23-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="c1e23-120">Startet ein Formular, um eine vorhandene Nachricht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c1e23-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="c1e23-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="c1e23-122">Eine Nachrichtenklasse in seiner Form innerhalb eines Containers Formular aufgelöst wird, und gibt ein Formular Informationen-Objekt für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="c1e23-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c1e23-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="c1e23-124">Eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.</span><span class="sxs-lookup"><span data-stu-id="c1e23-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c1e23-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="c1e23-126">Gibt ein Array von Eigenschaften, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1e23-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="c1e23-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="c1e23-128">Öffnet ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="c1e23-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="c1e23-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="c1e23-130">Zeigt ein Dialogfeld, mit dem den Benutzer ein Formular auswählen an und gibt ein Form-Informationen-Objekt, das dieses Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c1e23-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="c1e23-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="c1e23-132">Zeigt ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formular Informationsobjekten, die diesen Formularen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c1e23-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="c1e23-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="c1e23-134">Zeigt ein Dialogfeld an, die ermöglicht dem Benutzer das Formular Container auswählen, und gibt eine Schnittstelle für das Containerobjekt der ausgewählten Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="c1e23-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="c1e23-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="c1e23-136">Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für ein bestimmtes Formular Container.</span><span class="sxs-lookup"><span data-stu-id="c1e23-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="c1e23-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="c1e23-138">Downloads für ein Formular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c1e23-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="c1e23-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="c1e23-140">Bestimmt, ob ein Formular eine eigene Nachricht Konflikte verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1e23-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="c1e23-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c1e23-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="c1e23-142">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, auf das Formular-Manager-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c1e23-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1e23-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1e23-143">See also</span></span>



[<span data-ttu-id="c1e23-144">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c1e23-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

