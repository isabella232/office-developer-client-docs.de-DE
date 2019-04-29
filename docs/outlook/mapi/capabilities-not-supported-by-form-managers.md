---
title: Von Formular Managern nicht unterstützte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419380"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="5ff5b-103">Von Formular Managern nicht unterstützte Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ff5b-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="5ff5b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff5b-105">Die folgenden Features werden vom standardmäßigen Formular-Manager aus Leistungsgründen nicht unterstützt, können jedoch von benutzerdefinierten Formular-Managern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="5ff5b-106">Eine Hierarchie, die das Gruppieren oder Kategorisieren von Formularen in einer Formularbibliothek ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="5ff5b-107">Eine Formularbibliothek ist eine Flatfile-Datenbank mit Formularen.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="5ff5b-108">Zugriffssteuerung für Formular Kategorien, die Nachrichtenklassen oder übergeordneten Klassen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="5ff5b-109">Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="5ff5b-110">Dies sind Implementierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-110">These are implementation issues.</span></span> <span data-ttu-id="5ff5b-111">Es gibt nichts, was verhindert, dass ein benutzerdefinierter Formular-Manager diese Features implementiert.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="5ff5b-112">Die MAPI-Formulararchitektur unterstützt nicht mehrere Formular-Manager, die gleichzeitig laufen.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="5ff5b-113">Obwohl MAPI mehrere gleichzeitige Nachrichtenspeicher Anbieter, Transportanbieter und Adressbuchanbieter unterstützt, wird nur ein einziger Formular-Manager unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="5ff5b-114">Da möglicherweise nur ein Formular-Manager gleichzeitig gestartet wird, müssen Sie, wenn Sie einen benutzerdefinierten Formular-Manager implementieren, alle Funktionen aus dem standardmäßigen Formular-Manager, den Sie benötigen, erneut implementieren.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="5ff5b-115">Da Ihr benutzerdefinierter Formular-Manager den standardmäßigen Formular-Manager vollständig ersetzen wird, sind die Funktionen des Standardformular-Managers nur dann verfügbar, wenn Sie in Ihrem benutzerdefinierten Formular-Manager dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ff5b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ff5b-116">See also</span></span>



[<span data-ttu-id="5ff5b-117">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="5ff5b-117">MAPI Forms</span></span>](mapi-forms.md)

