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
ms.openlocfilehash: b53cdb4fe379405018555f1cca9fa40ddc5d0fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592486"
---
# <a name="mapi-forms"></a><span data-ttu-id="64f99-103">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="64f99-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="64f99-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64f99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64f99-105">Nach dem Lesen dieses Übersicht über die Architektur der MAPI-Formulars, müssen Sie einen Überblick über was MAPI-Formulare sind und Interaktion mit anderen Komponenten des MAPI-Subsystems.</span><span class="sxs-lookup"><span data-stu-id="64f99-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="64f99-106">Der Zweck dieses Abschnitts ist die grundlegende Kenntnisse zum Implementieren Ihrer eigenen MAPI Formular Server benötigten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="64f99-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="64f99-107">Vor dem Lesen dieses Abschnitts, sollten Sie sich mit dem Material im Thema [MAPI Workflowformulare (Übersicht)](mapi-forms-overview.md) vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="64f99-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="64f99-108">Weil die Architektur des MAPI-Formulars auf Component Object Model (COM) basiert, erfordert das Formular Server Anwendungsentwicklung Kenntnisse der COM-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="64f99-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="64f99-109">Weitere Informationen zu COM finden Sie im Abschnitt "COM und ActiveX-Objekt Services" im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="64f99-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

