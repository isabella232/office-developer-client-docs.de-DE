---
title: Abschnitt [Verbs] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583974"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="ad172-103">Abschnitt [Verbs] in der Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ad172-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="ad172-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad172-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad172-105">Im Abschnitt **[Verben]** wird der vollständige Satz von Verben, die vom Formular unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad172-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="ad172-106">Das Format des Abschnitts **[Verben]** lautet:</span><span class="sxs-lookup"><span data-stu-id="ad172-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="ad172-107">**[Verben]**</span><span class="sxs-lookup"><span data-stu-id="ad172-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="ad172-108">**Verb1** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="ad172-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="ad172-109">Es folgt ein Beispiel für einen Abschnitt **[Verben]** .</span><span class="sxs-lookup"><span data-stu-id="ad172-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="ad172-110">Jedes Verb definiert, in einer separaten **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="ad172-111">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="ad172-111">_string_ **]** section.</span></span> <span data-ttu-id="ad172-112">Eine **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-112">A **[Verb.**</span></span> <span data-ttu-id="ad172-113">_Zeichenfolge_ **]** Abschnitt beschreibt ein einzelnes Verb vom Formular angeboten.</span><span class="sxs-lookup"><span data-stu-id="ad172-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="ad172-114">Der Eintrag " **DisplayName** " in einem **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="ad172-115">_Zeichenfolge_ Abschnitt **]** gibt den Namen des Befehls in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad172-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="ad172-116">Der **Code** -Eintrag entspricht der Verbanzahl in der [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="ad172-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="ad172-117">Die Syntax für die **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="ad172-118">_Zeichenfolge_ **]** Abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="ad172-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="ad172-119">**[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-119">**[Verb.**</span></span> <span data-ttu-id="ad172-120">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="ad172-120">_string_ **]**</span></span>
  
 <span data-ttu-id="ad172-121">**DisplayName** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="ad172-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="ad172-122">**Code** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="ad172-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="ad172-123">**Flags** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="ad172-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="ad172-124">**Attributen** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="ad172-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="ad172-125">Nachfolgend sehen Sie ein Beispiel für eine **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ad172-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="ad172-126">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="ad172-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="ad172-127">In diesem Abschnitt aufgeführten Verben werden von einem Client mithilfe der [Methode IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad172-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="ad172-128">Verben aktiviert sind, indem das Formular [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode aufrufen, und übergeben sie die Anzahl von Code für die auszuführende Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad172-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

