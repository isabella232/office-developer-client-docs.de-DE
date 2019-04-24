---
title: Abschnitt "Formular Konfigurationsdatei [Erweiterungen]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327300"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="2de42-103">Abschnitt "Formular Konfigurationsdatei [Erweiterungen]"</span><span class="sxs-lookup"><span data-stu-id="2de42-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="2de42-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2de42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2de42-105">Im Abschnitt **[Extensions]** werden die erweiterten Attribute des Formulars aufgelistet, in der Regel ein benannter Eigenschaftensatz, bei dem es sich nicht um die grundlegenden Attribute handelt, die im Abschnitt **[Beschreibung]** der Formular Konfigurationsdatei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2de42-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="2de42-106">Erweiterte Attribute sind Eigenschaften, die von Aufrufen der \*\*\*\* GetProps-Methode des **IMAPIFormInfo** -Objekts zurückgegeben werden, wobei das High-Bit im Property-Tag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2de42-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="2de42-107">Client Anwendungen können die erweiterten Attribute eines Formulars bestimmen, sofern vorhanden, indem Sie diese Tags abrufen.</span><span class="sxs-lookup"><span data-stu-id="2de42-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="2de42-108">Dazu rufen die Clients die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode auf, übergeben die Namen der Eigenschaften des Formulars und rufen die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode auf, um die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2de42-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="2de42-109">**Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="2de42-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="2de42-110">**Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="2de42-110">**Extension.**</span></span> <span data-ttu-id="2de42-111">_string1_ =  _string2_</span><span class="sxs-lookup"><span data-stu-id="2de42-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="2de42-112">Jeder Abschnitt der Extension-Eigenschaft definiert ein Erweiterungsattribut mit der Syntax der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2de42-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="2de42-113">Der Eigenschaftentyp muss entweder PT_LONG oder PT_STRING8 sein.</span><span class="sxs-lookup"><span data-stu-id="2de42-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="2de42-114">Eigenschaftensätze mit benannten Zeichenfolgen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2de42-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="2de42-115">Das Format des Abschnitts **[Extension]** lautet:</span><span class="sxs-lookup"><span data-stu-id="2de42-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="2de42-116">**Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="2de42-116">**[Extension.**</span></span> <span data-ttu-id="2de42-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="2de42-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="2de42-118">**Typ** =  _Integer_</span><span class="sxs-lookup"><span data-stu-id="2de42-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="2de42-119">**NmidPropset** =  -_GUID_</span><span class="sxs-lookup"><span data-stu-id="2de42-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="2de42-120">**NmidInteger** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2de42-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="2de42-121">**Wert** =  __ String |  _Integer_</span><span class="sxs-lookup"><span data-stu-id="2de42-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="2de42-122">Es folgt ein Beispiel für einen **[Extensions]** -Abschnitt und einen nachfolgenden verwandten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="2de42-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


