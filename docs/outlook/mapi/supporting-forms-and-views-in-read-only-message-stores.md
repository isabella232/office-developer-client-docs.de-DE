---
title: Unterst�tzung von Formularen und Ansichten in nur-Lese Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432429"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="bff8a-103">Unterst�tzung von Formularen und Ansichten in nur-Lese Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="bff8a-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="bff8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bff8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bff8a-p101">Wenn Ihre Nachricht Speicheranbieter Lesezugriff auf die zugrunde liegende Speichermechanismus zul�sst, werden kann nicht zum Ausf�hren bestimmter Vorg�nge Client-Anwendungen und der MAPI-Formular-Manager. Insbesondere Clients k�nnen keine hinzuf�gen oder �ndern benutzerdefinierte Ansichten, und der MAPI-Formular-Manager k�nnen keine Formulare in den Tabellen zugeordneten Inhalt von Ordnern f�r den Speicher zu installieren.</span><span class="sxs-lookup"><span data-stu-id="bff8a-p101">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things. Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="bff8a-p102">F�r viele schreibgesch�tzte Nachricht Informationsspeicher, die ein Problem m�glicherweise nicht. Wenn dies der Fall ist, muss der Nachricht Informationsdienst nicht zugeordnete Inhalt Tabellen �berhaupt zu unterst�tzen. Wenn Ihre Nachricht Speicheranbieter schreibgesch�tzt sein muss, und es muss auch eine vordefinierte Reihe von Ansichten oder Formulare unterst�tzen, m�ssen sie zur Unterst�tzung von Tabellen zugeordneten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="bff8a-p102">For many read-only message stores, that may not be a problem. If that is the case, the message store provider does not need to support associated contents tables at all. However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="bff8a-p103">Die am h�ufigsten verwendete Strategie zum, da dadurch Clients und der MAPI-Formular-Manager k�nnen nicht die Ansichten zu installieren oder Speichern von Formularen in die Nachricht selbst ist f�r die Nachricht Speicheranbieter vordefinierten Code sie in der Nachrichtenspeicher. Dies bedeutet, dass die zugeh�rigen Inhaltstabelle oder Tabellen, die Sichten oder -Formulare enthalten, im Nachrichtenspeicher vorhanden werden, bei der Erstellung, bevor Clients oder der MAPI-Formular-Manager jemals darauf zugreifen. Klicken Sie, wenn ein Client eine zugeordnete Inhaltstabelle zum Abrufen von benutzerdefinierter Ansichten von einem Formular fordert oder der MAPI-Formular-Manager eine zugeordnete Inhaltstabelle fordert um ein Formular zu starten, der Nachricht Store Anbieter eine bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="bff8a-p103">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store. This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it. Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="bff8a-p104">Dadurch, dass die zugeh�rigen Inhalt Tabellen erstellt und aufgef�llt, wenn der Nachrichtenspeicher selbst erstellt wird impliziert, dass Ihre Nachricht Speicheranbieter ben�tigen, Informationen zum Format der speziellen Nachrichten zu erhalten, dass Clients und der MAPI-Manager verwenden Sie zum Speichern von Datenansichten und Formularen bilden. Was sind diese Formate richtet sich nach dem Client und MAPI-Formular-Manager verwendet wird, damit eine Beschreibung f�r diese hier bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bff8a-p104">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms. What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bff8a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff8a-115">See also</span></span>



[<span data-ttu-id="bff8a-116">Read-Only Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="bff8a-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

