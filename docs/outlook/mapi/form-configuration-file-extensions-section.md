---
title: Abschnitt [Extensions] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791703"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="4b3e2-103">Abschnitt [Extensions] in der Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="4b3e2-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="4b3e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b3e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b3e2-105">Der Abschnitt **[Extensions]** Listet die erweiterten Attribute des Formulars, in der Regel eine benannte Eigenschaft festgelegt, die alle außer den grundlegenden in den Abschnitt **[Beschreibung]** der Konfigurationsdatei Formular aufgeführten Attribute sind.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="4b3e2-106">Erweiterte Attribute sind Eigenschaften von Aufrufe der **GetProps** -Methode des **IMAPIFormInfo** -Objekts zurückgegeben wird, mit dem hohe Bit in das Eigenschafts-Tag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="4b3e2-107">Clientanwendungen können erweiterte Attribute eines Formulars, gegebenenfalls durch diese Tags abrufen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="4b3e2-108">Dazu Clients rufen Sie die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode und die Namen der Eigenschaften des Formulars übergeben, und rufen die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="4b3e2-109">**[Extensions]**</span><span class="sxs-lookup"><span data-stu-id="4b3e2-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="4b3e2-110">**Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="4b3e2-110">**Extension.**</span></span> <span data-ttu-id="4b3e2-111">_String1_ =  _string2_</span><span class="sxs-lookup"><span data-stu-id="4b3e2-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="4b3e2-112">Jede Erweiterung-Eigenschaft im Abschnitt definiert eine von der mit dem Namen Eigenschaftensyntax MAPI Extension-Attribut.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="4b3e2-113">Der Eigenschaftentyp muss PT_LONG oder PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="4b3e2-114">Eigenschaftensätze, die benannte Zeichenfolgen enthält, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="4b3e2-115">Das Format des Abschnitts **[Erweiterung]** lautet:</span><span class="sxs-lookup"><span data-stu-id="4b3e2-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="4b3e2-116">**[Erweiterung.**</span><span class="sxs-lookup"><span data-stu-id="4b3e2-116">**[Extension.**</span></span> <span data-ttu-id="4b3e2-117">_Zeichenfolge2_ **]**</span><span class="sxs-lookup"><span data-stu-id="4b3e2-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="4b3e2-118">**Typ** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="4b3e2-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="4b3e2-119">**NmidPropset** =  _Guid_</span><span class="sxs-lookup"><span data-stu-id="4b3e2-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="4b3e2-120">**NmidInteger** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="4b3e2-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="4b3e2-121">**Wert** =  _Zeichenfolge_ |  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="4b3e2-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="4b3e2-122">Ein Beispiel für einen Abschnitt **[Extensions]** und einer der folgenden Verwandte Abschnitte wird nach angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b3e2-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


