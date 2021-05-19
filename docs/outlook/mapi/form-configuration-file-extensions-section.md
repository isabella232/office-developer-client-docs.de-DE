---
title: Abschnitt "Formularkonfigurationsdatei [ Erweiterungen]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423755"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="264d8-103">Abschnitt "Formularkonfigurationsdatei [ Erweiterungen]</span><span class="sxs-lookup"><span data-stu-id="264d8-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="264d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="264d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="264d8-105">Im **Abschnitt [Extensions]** werden die erweiterten Attribute des Formulars aufgelistet, in der Regel ein benannter Eigenschaftensatz, bei dem es sich um Attribute handelt, die über die grundlegenden Attribute hinausgehen, die im **Abschnitt [Beschreibung]** der Formularkonfigurationsdatei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="264d8-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="264d8-106">Erweiterte Attribute sind Eigenschaften, die von Aufrufen an die **GetProps-Methode** des **IMAPIFormInfo-Objekts** zurückgegeben werden, deren High-Bit im Eigenschaftstag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="264d8-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="264d8-107">Clientanwendungen können die erweiterten Attribute eines Formulars bestimmen, sofern dies der Fall ist, indem diese Tags abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="264d8-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="264d8-108">Dazu rufen Clients die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) auf, übergeben die Namen der Eigenschaften des Formulars und rufen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um die Eigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="264d8-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="264d8-109">**[Erweiterungen]**</span><span class="sxs-lookup"><span data-stu-id="264d8-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="264d8-110">**Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="264d8-110">**Extension.**</span></span> <span data-ttu-id="264d8-111">_string1_  =   _string2_</span><span class="sxs-lookup"><span data-stu-id="264d8-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="264d8-112">Jeder Abschnitt der Erweiterungseigenschaft definiert ein Erweiterungsattribut mithilfe der SYNTAX der benannten MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="264d8-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="264d8-113">Der Eigenschaftentyp muss entweder PT_LONG oder PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="264d8-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="264d8-114">Eigenschaftssätze, die benannte Zeichenfolgen enthalten, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="264d8-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="264d8-115">Das Format des **Abschnitts [Extension]** ist:</span><span class="sxs-lookup"><span data-stu-id="264d8-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="264d8-116">**[Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="264d8-116">**[Extension.**</span></span> <span data-ttu-id="264d8-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="264d8-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="264d8-118">**Type**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="264d8-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="264d8-119">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="264d8-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="264d8-120">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="264d8-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="264d8-121">**Wert**  =   _string_  |   _integer_</span><span class="sxs-lookup"><span data-stu-id="264d8-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="264d8-122">Nachfolgend finden Sie ein Beispiel für einen **Abschnitt [Extensions]** und einen nachfolgenden verwandten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="264d8-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


