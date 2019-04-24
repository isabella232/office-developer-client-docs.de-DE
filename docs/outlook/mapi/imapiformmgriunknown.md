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
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321651"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="3a872-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a872-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="3a872-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a872-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a872-105">Ermöglicht es den Formular Viewern, Informationen über Formularserver zu erhalten und zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a872-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a872-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3a872-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a872-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="3a872-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="3a872-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="3a872-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a872-109">Formular-Manager-Objekte</span><span class="sxs-lookup"><span data-stu-id="3a872-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="3a872-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3a872-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a872-111">Formular Bibliotheks Anbieter</span><span class="sxs-lookup"><span data-stu-id="3a872-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="3a872-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3a872-112">Called by:</span></span>  <br/> |<span data-ttu-id="3a872-113">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="3a872-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="3a872-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="3a872-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a872-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="3a872-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="3a872-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="3a872-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a872-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="3a872-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a872-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="3a872-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a872-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="3a872-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="3a872-120">Startet ein Formular zum Öffnen einer vorhandenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3a872-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="3a872-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3a872-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="3a872-122">Löst eine Nachrichtenklasse in Ihrem Formular innerhalb eines Formular Containers auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="3a872-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="3a872-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="3a872-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="3a872-124">Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare innerhalb eines Formular Containers auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="3a872-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="3a872-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="3a872-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="3a872-126">Gibt ein Array der Eigenschaften zurück, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a872-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="3a872-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="3a872-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="3a872-128">Startet ein Formular zum Erstellen einer neuen Nachricht auf der Grundlage der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="3a872-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="3a872-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="3a872-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="3a872-130">Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen und ein Formular Informationsobjekt zurückgibt, das dieses Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3a872-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="3a872-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="3a872-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="3a872-132">Zeigt ein Dialogfeld an, in dem der Benutzer mehrere Formulare auswählen kann, und es wird ein Array von Formular Informationsobjekten zurückgegeben, die diese Formulare beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3a872-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="3a872-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="3a872-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="3a872-134">Zeigt ein Dialogfeld an, in dem der Benutzer einen Formular Container auswählen und eine Schnittstelle für das Containerobjekt zurückgibt, das der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="3a872-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="3a872-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="3a872-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="3a872-136">Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für einen bestimmten Formular Container.</span><span class="sxs-lookup"><span data-stu-id="3a872-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="3a872-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="3a872-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="3a872-138">Lädt ein Formular zum Öffnen herunter.</span><span class="sxs-lookup"><span data-stu-id="3a872-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="3a872-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="3a872-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="3a872-140">Bestimmt, ob ein Formular eigene Nachrichten Konflikte verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="3a872-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="3a872-141">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="3a872-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="3a872-142">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Formular-Manager-Objekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="3a872-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a872-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a872-143">See also</span></span>



[<span data-ttu-id="3a872-144">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3a872-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

