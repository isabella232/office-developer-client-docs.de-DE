---
title: MAPI-Formular-Manager
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792983"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="477f3-103">MAPI-Formular-Manager</span><span class="sxs-lookup"><span data-stu-id="477f3-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="477f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="477f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="477f3-105">Ein Formular-Manager ist ein Objekt, das die [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="477f3-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="477f3-106">Die meisten Organisationen verwenden den Formular-Manager Lieferumfang MAPI, als der Standard-Formular-Manager bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="477f3-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="477f3-107">Jedoch kann eine Organisation den Standard-Formular-Manager mit einem benutzerdefinierten Formular-Manager ersetzen, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="477f3-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="477f3-108">Der Formular-Manager kümmert Auffinden von Formularen in Formularbibliotheken, Laden von Formularen in Reaktion auf Benutzeranfragen und Formulare in lokalen Formularbibliothek, Ordner-Formularbibliothek oder persönliche Formularbibliothek des Benutzers installieren.</span><span class="sxs-lookup"><span data-stu-id="477f3-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="477f3-109">Für einen Benutzer für die Interaktion mit einer Meldung muss eine Instanz des Servers für die Nachricht Nachrichtenklasse Formular erstellt und aktiviert, um die Meldung angezeigt, und führen Sie den angeforderten Vorgang für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="477f3-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="477f3-110">Wie im Thema [MAPI Formularbibliotheken](mapi-form-libraries.md)beschrieben, kann Implementierung eines Formulars an unterschiedlichen Speicherorten (Formularbibliotheken) vorhanden und kann nicht garantiert, dass ein Formular oder der entsprechende Server lokal verfügbar sein oder in einer laufenden, wenn Benutzer angeben für die Interaktion wird mit diesem.</span><span class="sxs-lookup"><span data-stu-id="477f3-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="477f3-111">Der Formular-Manager sorgt für ausführliche Informationen zu suchen und aktivieren das Formular.</span><span class="sxs-lookup"><span data-stu-id="477f3-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="477f3-112">Clients verwenden von der Formular-Manager bereitgestellten Dienste zum Suchen und Aktivieren von Formularen.</span><span class="sxs-lookup"><span data-stu-id="477f3-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="477f3-113">Die **IMAPIFormMgr** -Schnittstelle wird von der Formular-Manager implementiert und von Clients für den Zugriff auf seine Services aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="477f3-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="477f3-114">Der Formular-Manager ist ein wesentlicher Bestandteil, da es fast alle Details der suchen und Aktivieren von Formularen von messaging-Clients werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="477f3-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="477f3-115">Formular Servern zu laden, lädt der Standard-Formular-Manager das Formular aus der ersten Formularbibliothek, in der Sie eine Implementierung für die Nachrichtenklasse des Formulars befindet.</span><span class="sxs-lookup"><span data-stu-id="477f3-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="477f3-116">Der Standard-Formular-Manager sucht die Formularbibliotheken in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="477f3-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="477f3-117">Lokale Formularbibliothek des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="477f3-117">The user's local form library.</span></span> <span data-ttu-id="477f3-118">Diese Formularbibliothek wird zuerst durchsucht, da es den schnellsten Zugriff auf die Implementierung eines Formulars bereitstellt, wenn die Implementierung in der lokalen Formularbibliothek installiert ist.</span><span class="sxs-lookup"><span data-stu-id="477f3-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="477f3-119">Der Ordner-Formularbibliothek die Nachricht Containers – der Ordner, in dem die Nachricht geladene gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="477f3-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="477f3-120">Der Benutzer Persönliche Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="477f3-120">The user's personal form library.</span></span>
    
<span data-ttu-id="477f3-121">Ein benutzerdefiniertes Formular-Manager kann die verfügbaren Formularbibliotheken in beliebiger Reihenfolge suchen oder anderen Formularbibliotheken wie etwa einer Organisation geltende Formularbibliothek implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="477f3-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="477f3-122">Weitere Informationen zu Formularbibliotheken finden Sie unter [MAPI Formularbibliotheken](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="477f3-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="477f3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="477f3-123">See also</span></span>



[<span data-ttu-id="477f3-124">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="477f3-124">MAPI Forms</span></span>](mapi-forms.md)

