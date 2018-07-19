---
title: Von Formularmanagern nicht unterstützte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791371"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="3b35e-103">Von Formularmanagern nicht unterstützte Funktionen</span><span class="sxs-lookup"><span data-stu-id="3b35e-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="3b35e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b35e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b35e-105">Die folgenden Features werden von der Standard-Formular-Manager aus Gründen der Systemleistung nicht unterstützt, aber können benutzerdefiniertes Formular-Manager unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3b35e-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="3b35e-106">Eine Hierarchie, mit die Formulare gruppiert oder in einer Formularbibliothek kategorisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b35e-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="3b35e-107">Eine Formularbibliothek bietet eine Flatfile Datenbank von Formularen.</span><span class="sxs-lookup"><span data-stu-id="3b35e-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="3b35e-108">Steuerung des Zugriffs für Kategorien von Formularen, Nachrichtenklassen oder Klassen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3b35e-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="3b35e-109">Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="3b35e-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="3b35e-110">Dies sind die Implementierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="3b35e-110">These are implementation issues.</span></span> <span data-ttu-id="3b35e-111">Es gibt nichts zu verhindern, dass einen benutzerdefiniertes Formular-Manager Implementieren dieser Features.</span><span class="sxs-lookup"><span data-stu-id="3b35e-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="3b35e-112">Die MAPI-Formular-Architektur bietet keine Unterstützung für mehrere Formular-Manager werden gleichzeitig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b35e-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="3b35e-113">Obwohl MAPI mehrere gleichzeitige Nachricht-Anbieter, Transport Provider und adressbuchanbietern implementierte unterstützt, wird nur ein einzelnes Formular-Manager unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b35e-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="3b35e-114">Da nur ein Formular-Manager auf einmal ausgeführt werden kann, wenn Sie einen benutzerdefiniertes Formular-Manager implementieren müssen Sie alle Funktionen aus der Standard-Formular-Manager erneut zu implementieren, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="3b35e-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="3b35e-115">Da Ihr benutzerdefiniertes Formular-Manager den Standard-Formular-Manager vollständig ersetzt werden sollen, werden Funktionen von der Standard-Formular-Manager nicht verfügbar, es sei denn, sie in Ihrem benutzerdefinierten Formular-Manager dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3b35e-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3b35e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b35e-116">See also</span></span>



[<span data-ttu-id="3b35e-117">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="3b35e-117">MAPI Forms</span></span>](mapi-forms.md)

