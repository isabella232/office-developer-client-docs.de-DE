---
title: MAPI-Formulare
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351345"
---
# <a name="mapi-forms"></a><span data-ttu-id="df186-103">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="df186-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="df186-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df186-105">Nach der Lektüre dieser Übersicht über die MAPI-Formulararchitektur haben Sie Verständnis dafür, was MAPI-Formulare sind und wie Sie mit anderen Komponenten des MAPI-Subsystems interagieren.</span><span class="sxs-lookup"><span data-stu-id="df186-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="df186-106">Dieser Abschnitt soll Ihnen die konzeptionellen Kenntnisse vermitteln, die Sie benötigen, um Ihre eigenen MAPI-Formularserver zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="df186-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="df186-107">Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit dem Material im Thema [MAPI Forms Overview](mapi-forms-overview.md) vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="df186-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="df186-108">Da die MAPI-Formulararchitektur auf dem Component Object Model (COM) basiert, erfordert das Entwickeln von Formularserver Anwendungen Kenntnisse der COM-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="df186-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="df186-109">Weitere Informationen zu COM finden Sie im Abschnitt COM-und ActiveX-Objektdienste im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="df186-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

