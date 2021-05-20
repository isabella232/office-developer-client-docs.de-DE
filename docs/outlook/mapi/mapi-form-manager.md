---
title: MAPI-Formular-Manager
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430196"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="3707b-103">MAPI-Formular-Manager</span><span class="sxs-lookup"><span data-stu-id="3707b-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="3707b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3707b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3707b-105">Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr-Schnittstelle](imapiformmgriunknown.md) implementiert.</span><span class="sxs-lookup"><span data-stu-id="3707b-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="3707b-106">Die meisten Organisationen verwenden den mit MAPI bereitgestellten Formular-Manager, der als Standardformular-Manager bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3707b-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="3707b-107">Eine Organisation kann jedoch bei Bedarf den Standardformular-Manager durch einen benutzerdefinierten Formular-Manager ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3707b-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="3707b-108">Der Formular-Manager kümmert sich um das Suchen von Formularen in Formularbibliotheken, das Laden von Formularen als Reaktion auf Benutzeranforderungen und das Installieren von Formularen in der lokalen Formularbibliothek, der Ordnerformularbibliothek oder der persönlichen Formularbibliothek eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3707b-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="3707b-109">Damit ein Benutzer mit einer Nachricht interagieren kann, muss eine Instanz des Formularservers für die Nachrichtenklasse der Nachricht erstellt und aktiviert werden, um die Nachricht anzeigen und den angeforderten Vorgang für die Nachricht durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="3707b-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="3707b-110">Wie im Thema [MAPI-Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann die Implementierung eines Formulars an mehreren verschiedenen Speicherorten (Formularbibliotheken) vorhanden sein, und es gibt keine Garantie, dass ein Formular oder sein Server lokal verfügbar ist oder sich in einem ausgeführten Zustand befindet, wenn ein Benutzer mit ihm interagieren möchte.</span><span class="sxs-lookup"><span data-stu-id="3707b-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="3707b-111">Der Formularmanager kümmert sich um die Details des Suchens und Aktivierens des Formulars.</span><span class="sxs-lookup"><span data-stu-id="3707b-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="3707b-112">Clients verwenden Dienste, die vom Formular-Manager bereitgestellt werden, um Formulare zu finden und zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3707b-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="3707b-113">Die **IMAPIFormMgr-Schnittstelle** wird vom Formular-Manager implementiert und von Clients aufgerufen, um auf die Dienste zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3707b-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="3707b-114">Der Formular-Manager ist eine wesentliche Komponente, da er fast alle Details zum Suchen und Aktivieren von Formularen in Messagingclients ausblendet.</span><span class="sxs-lookup"><span data-stu-id="3707b-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="3707b-115">Beim Laden von Formularservern lädt der Standardformular-Manager das Formular aus der ersten Formularbibliothek, in der eine Implementierung für die Nachrichtenklasse des Formulars gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="3707b-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="3707b-116">Der Standardformular-Manager durchsucht die Formularbibliotheken in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="3707b-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="3707b-117">Die lokale Formularbibliothek des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3707b-117">The user's local form library.</span></span> <span data-ttu-id="3707b-118">Diese Formularbibliothek wird zuerst durchsucht, da sie den schnellsten Zugriff auf die Implementierung eines Formulars bietet, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3707b-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="3707b-119">Die Ordnerformularbibliothek des Nachrichtencontainers – der Ordner, in dem die zu ladende Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3707b-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="3707b-120">Die persönliche Formularbibliothek des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3707b-120">The user's personal form library.</span></span>
    
<span data-ttu-id="3707b-121">Ein benutzerdefinierter Formular-Manager kann die verfügbaren Formularbibliotheken in beliebiger Reihenfolge durchsuchen oder andere Formularbibliotheken implementieren, z. B. eine organisationsweite Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="3707b-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="3707b-122">Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI Form Libraries](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="3707b-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3707b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3707b-123">See also</span></span>



[<span data-ttu-id="3707b-124">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="3707b-124">MAPI Forms</span></span>](mapi-forms.md)

