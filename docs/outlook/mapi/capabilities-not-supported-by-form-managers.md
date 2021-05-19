---
title: Funktionen, die von Formularmanagern nicht unterstützt werden
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
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="0665c-103">Funktionen, die von Formularmanagern nicht unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="0665c-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="0665c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0665c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0665c-105">Die folgenden Features werden vom Standardmäßigen Formular-Manager aus Leistungsgründen nicht unterstützt, können jedoch von benutzerdefinierten Formularmanagern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0665c-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="0665c-106">Eine Hierarchie, die das Gruppieren oder Kategorisieren von Formularen in einer Formularbibliothek ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0665c-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="0665c-107">Eine Formularbibliothek ist eine Flachdateidatenbank von Formularen.</span><span class="sxs-lookup"><span data-stu-id="0665c-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="0665c-108">Zugriffssteuerung für Formularkategorien, die Nachrichtenklassen oder Superklassen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0665c-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="0665c-109">Unterstützung für mehrere Sprachversionen desselben Formulars in einer einzelnen Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="0665c-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="0665c-110">Dies sind Implementierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="0665c-110">These are implementation issues.</span></span> <span data-ttu-id="0665c-111">Es gibt nichts, was einen benutzerdefinierten Formular-Manager daran hindern kann, diese Features zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="0665c-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="0665c-112">Die MAPI-Formulararchitektur unterstützt nicht mehrere Formularmanager, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0665c-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="0665c-113">Obwohl MAPI mehrere gleichzeitige Nachrichtenspeicheranbieter, Transportanbieter und Adressbuchanbieter unterstützt, wird nur ein einzelner Formular-Manager unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0665c-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="0665c-114">Da möglicherweise nur ein Formular-Manager gleichzeitig ausgeführt wird, müssen Sie beim Implementieren eines benutzerdefinierten Formular-Managers alle benötigten Funktionen aus dem Standardformular-Manager neu implementieren.</span><span class="sxs-lookup"><span data-stu-id="0665c-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="0665c-115">Da ihr benutzerdefinierter Formular-Manager den Standardformular-Manager vollständig ersetzt, stehen Funktionen des Standardformular-Managers nicht zur Verfügung, es sei denn, sie werden im benutzerdefinierten Formular-Manager dupliziert.</span><span class="sxs-lookup"><span data-stu-id="0665c-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0665c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0665c-116">See also</span></span>



[<span data-ttu-id="0665c-117">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="0665c-117">MAPI Forms</span></span>](mapi-forms.md)

