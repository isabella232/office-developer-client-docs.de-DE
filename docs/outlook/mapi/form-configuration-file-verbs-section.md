---
title: Formular Konfigurationsdatei [Verbs] Abschnitt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327496"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="45120-103">Formular Konfigurationsdatei [Verbs] Abschnitt</span><span class="sxs-lookup"><span data-stu-id="45120-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="45120-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45120-105">Der Abschnitt **[Verbs]** enthält die vollständigen Verben, die vom Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="45120-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="45120-106">Das Format des Abschnitts **[Verbs]** lautet:</span><span class="sxs-lookup"><span data-stu-id="45120-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="45120-107">**Verben**</span><span class="sxs-lookup"><span data-stu-id="45120-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="45120-108">**Verb1** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="45120-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="45120-109">Es folgt ein Beispiel für einen Abschnitt **[Verbs]** .</span><span class="sxs-lookup"><span data-stu-id="45120-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="45120-110">Jedes Verb wird in einem separaten **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="45120-111">_Zeichenfolge_ **]** -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="45120-111">_string_ **]** section.</span></span> <span data-ttu-id="45120-112">Ein **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-112">A **[Verb.**</span></span> <span data-ttu-id="45120-113">_Zeichenfolge_ **]** section beschreibt ein einzelnes Verb, das vom Formular angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="45120-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="45120-114">Der Eintrag **DisplayName** in einem **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="45120-115">_Zeichenfolge_ **]** -Abschnitt gibt den in der Benutzeroberfläche angezeigten Befehlsnamen an.</span><span class="sxs-lookup"><span data-stu-id="45120-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="45120-116">Der **Code** Eintrag entspricht der Verb Nummer, die in der [IMAPIForm::D overb](imapiform-doverb.md) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="45120-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="45120-117">Die Syntax für das **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="45120-118">_Zeichenfolge_ **]** section ist:</span><span class="sxs-lookup"><span data-stu-id="45120-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="45120-119">**Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-119">**[Verb.**</span></span> <span data-ttu-id="45120-120">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="45120-120">_string_ **]**</span></span>
  
 <span data-ttu-id="45120-121">\*\*\*\* Angezeigte Zeichen_Folge_  =  </span><span class="sxs-lookup"><span data-stu-id="45120-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="45120-122">**Code** =  _Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="45120-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="45120-123">**Flags** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="45120-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="45120-124">**Attribute** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="45120-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="45120-125">Es folgt ein Beispiel für ein **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="45120-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="45120-126">_Zeichenfolge_ **]** -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="45120-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="45120-127">Verben, die in diesem Abschnitt aufgelistet werden, werden von einem Client mithilfe der [IMAPIFormInfo:: CalcVerbSet-Methode](imapiforminfo-calcverbset.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="45120-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="45120-128">Verben werden aktiviert, indem die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Formulars aufgerufen und die Codenummer des auszuführenden Verbs übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="45120-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

