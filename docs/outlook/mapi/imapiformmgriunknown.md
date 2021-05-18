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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413059"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="5aa43-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5aa43-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="5aa43-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5aa43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5aa43-105">Ermöglicht Formularanzeigen, Informationen zu Formularservern zu erhalten und zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5aa43-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5aa43-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5aa43-106">Header file:</span></span>  <br/> |<span data-ttu-id="5aa43-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="5aa43-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5aa43-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="5aa43-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5aa43-109">Form-Manager-Objekte</span><span class="sxs-lookup"><span data-stu-id="5aa43-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="5aa43-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5aa43-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5aa43-111">Anbieter von Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="5aa43-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="5aa43-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5aa43-112">Called by:</span></span>  <br/> |<span data-ttu-id="5aa43-113">Formularanzeigen</span><span class="sxs-lookup"><span data-stu-id="5aa43-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="5aa43-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="5aa43-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5aa43-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="5aa43-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="5aa43-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="5aa43-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5aa43-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="5aa43-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5aa43-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5aa43-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5aa43-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="5aa43-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="5aa43-120">Startet ein Formular zum Öffnen einer vorhandenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5aa43-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="5aa43-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="5aa43-122">Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa43-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5aa43-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="5aa43-124">Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa43-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="5aa43-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="5aa43-126">Gibt ein Array der Eigenschaften zurück, die von einer Gruppe von Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5aa43-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="5aa43-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="5aa43-128">Startet ein Formular, um eine neue Nachricht basierend auf der Nachrichtenklasse des Formulars zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5aa43-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="5aa43-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="5aa43-130">Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen kann, und gibt ein Formularinformationsobjekt zurück, das dieses Formular beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5aa43-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="5aa43-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="5aa43-132">Stellt ein Dialogfeld vor, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5aa43-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="5aa43-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="5aa43-134">Zeigt ein Dialogfeld an, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa43-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="5aa43-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="5aa43-136">Öffnet eine [IMAPIFormContainer-Schnittstelle](imapiformcontaineriunknown.md) für einen bestimmten Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="5aa43-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="5aa43-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="5aa43-138">Lädt ein Formular zum Öffnen herunter.</span><span class="sxs-lookup"><span data-stu-id="5aa43-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="5aa43-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="5aa43-140">Bestimmt, ob ein Formular eigene Nachrichtenkonflikte verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5aa43-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="5aa43-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5aa43-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="5aa43-142">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formular-Manager-Objekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5aa43-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5aa43-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aa43-143">See also</span></span>



[<span data-ttu-id="5aa43-144">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5aa43-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

