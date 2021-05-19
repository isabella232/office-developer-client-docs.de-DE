---
title: Abschnitt "Formularkonfigurationsdatei" [Verben]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417784"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="ffad3-103">Abschnitt "Formularkonfigurationsdatei" [Verben]</span><span class="sxs-lookup"><span data-stu-id="ffad3-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="ffad3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffad3-105">Im **Abschnitt [Verben]** werden die vollständigen Verben aufgeführt, die vom Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ffad3-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="ffad3-106">Das Format des **Abschnitts [Verben]** ist:</span><span class="sxs-lookup"><span data-stu-id="ffad3-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="ffad3-107">**[Verben]**</span><span class="sxs-lookup"><span data-stu-id="ffad3-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="ffad3-108">**Verb1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="ffad3-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="ffad3-109">Im Folgenden finden Sie ein Beispiel für einen **[Verbs]-Abschnitt.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="ffad3-110">Jedes Verb ist in einem separaten **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="ffad3-111">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="ffad3-111">_string_ **]** section.</span></span> <span data-ttu-id="ffad3-112">A **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-112">A **[Verb.**</span></span> <span data-ttu-id="ffad3-113">_Im Abschnitt string_ **]** wird ein einzelnes Verb beschrieben, das vom Formular angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="ffad3-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="ffad3-114">Der **Eintrag DisplayName** in einem **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="ffad3-115">_string_ **]** -Abschnitt gibt den Befehlsnamen an, der auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ffad3-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="ffad3-116">Der **Code-Eintrag** entspricht der Verbnummer, die in der [IMAPIForm::D oVerb-Methode übergeben](imapiform-doverb.md) wird.</span><span class="sxs-lookup"><span data-stu-id="ffad3-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="ffad3-117">Die Syntax für **das [Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="ffad3-118">_string_ **]** section is:</span><span class="sxs-lookup"><span data-stu-id="ffad3-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="ffad3-119">**[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-119">**[Verb.**</span></span> <span data-ttu-id="ffad3-120">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="ffad3-120">_string_ **]**</span></span>
  
 <span data-ttu-id="ffad3-121">**DisplayName**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="ffad3-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="ffad3-122">**Code**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="ffad3-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="ffad3-123">**Flags**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="ffad3-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="ffad3-124">**Attribs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="ffad3-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="ffad3-125">Im Folgenden finden Sie ein Beispiel für **ein [Verb.**</span><span class="sxs-lookup"><span data-stu-id="ffad3-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="ffad3-126">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="ffad3-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="ffad3-127">In diesem Abschnitt aufgeführte Verben werden von einem Client mithilfe der [IMAPIFormInfo::CalcVerbSet-Methode abgerufen.](imapiforminfo-calcverbset.md)</span><span class="sxs-lookup"><span data-stu-id="ffad3-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="ffad3-128">Verben werden aktiviert, indem die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars aufruft und die Codenummer des verb übergeben wird, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffad3-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

