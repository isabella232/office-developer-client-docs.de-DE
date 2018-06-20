---
title: Formular Konfigurationsabschnitt Datei [Verben]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791720"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="c1407-103">Formular Konfigurationsabschnitt Datei [Verben]</span><span class="sxs-lookup"><span data-stu-id="c1407-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="c1407-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1407-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1407-105">Im Abschnitt **[Verben]** wird der vollständige Satz von Verben, die vom Formular unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1407-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="c1407-106">Das Format des Abschnitts **[Verben]** lautet:</span><span class="sxs-lookup"><span data-stu-id="c1407-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="c1407-107">**[Verben]**</span><span class="sxs-lookup"><span data-stu-id="c1407-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="c1407-108">**Verb1** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="c1407-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="c1407-109">Es folgt ein Beispiel für einen Abschnitt **[Verben]** .</span><span class="sxs-lookup"><span data-stu-id="c1407-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="c1407-110">Jedes Verb definiert, in einer separaten **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="c1407-111">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="c1407-111">_string_ **]** section.</span></span> <span data-ttu-id="c1407-112">Eine **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-112">A **[Verb.**</span></span> <span data-ttu-id="c1407-113">_Zeichenfolge_ **]** Abschnitt beschreibt ein einzelnes Verb vom Formular angeboten.</span><span class="sxs-lookup"><span data-stu-id="c1407-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="c1407-114">Der Eintrag " **DisplayName** " in einem **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="c1407-115">_Zeichenfolge_ Abschnitt **]** gibt den Namen des Befehls in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1407-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="c1407-116">Der **Code** -Eintrag entspricht der Verbanzahl in der [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="c1407-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="c1407-117">Die Syntax für die **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="c1407-118">_Zeichenfolge_ **]** Abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="c1407-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="c1407-119">**[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-119">**[Verb.**</span></span> <span data-ttu-id="c1407-120">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="c1407-120">_string_ **]**</span></span>
  
 <span data-ttu-id="c1407-121">**DisplayName** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="c1407-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="c1407-122">**Code** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="c1407-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="c1407-123">**Flags** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="c1407-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="c1407-124">**Attributen** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="c1407-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="c1407-125">Nachfolgend sehen Sie ein Beispiel für eine **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="c1407-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="c1407-126">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="c1407-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="c1407-127">In diesem Abschnitt aufgeführten Verben werden von einem Client mithilfe der [Methode IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c1407-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="c1407-128">Verben aktiviert sind, indem das Formular [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode aufrufen, und übergeben sie die Anzahl von Code für die auszuführende Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c1407-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

