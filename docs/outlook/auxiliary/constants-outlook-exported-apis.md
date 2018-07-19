---
title: Konstanten (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Dieses Thema enthält Konstantendefinitionen für APIs, die Outlook exportiert.
ms.openlocfilehash: 54b491e436b7b9275a227de40439ddb66d8d0c5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790927"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="a4b7b-103">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="a4b7b-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="a4b7b-104">Dieses Thema enthält Konstantendefinitionen für APIs, die Outlook exportiert.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="a4b7b-105">Unterstützung von Definitionen für Zeitzone</span><span class="sxs-lookup"><span data-stu-id="a4b7b-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="a4b7b-106">Unterstützung von Definitionen für Kategorie</span><span class="sxs-lookup"><span data-stu-id="a4b7b-106">Definitions for Category support</span></span>

|<span data-ttu-id="a4b7b-107">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-107">**Constant**</span></span>|<span data-ttu-id="a4b7b-108">**Definition**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4b7b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a4b7b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="a4b7b-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4b7b-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="a4b7b-111">Sonstige Versendung-IDs</span><span class="sxs-lookup"><span data-stu-id="a4b7b-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="a4b7b-112">Outlook macht die folgenden Versendung-IDs (Dispids) verfügbar, sodass Entwickler [IDispatch:: Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) verwenden können, um Zugriff auf die entsprechende Eigenschaft oder Methode oder die entsprechenden Ereignis überwachen.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="a4b7b-113">**Zugehörige Konstante**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-113">**Associated constant**</span></span>|<span data-ttu-id="a4b7b-114">**DISPID-Wert**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-114">**Dispid value**</span></span>|<span data-ttu-id="a4b7b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-115">**Description**</span></span>|<span data-ttu-id="a4b7b-116">**Zutreffend-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4b7b-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="a4b7b-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="a4b7b-118">0xF024</span></span>  <br/> |<span data-ttu-id="a4b7b-119">Zum Aufrufen der entsprechenden Eigenschaft für ein Element wird überprüft, ob das Element wurde geändert, aber nicht gespeichert wurde verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="a4b7b-120">Objekte auf Elementebene</span><span class="sxs-lookup"><span data-stu-id="a4b7b-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="a4b7b-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="a4b7b-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="a4b7b-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="a4b7b-123">Verwendet, um die entsprechende Methode in der Explorer oder Inspektor, um anzugeben, ob das Bild eines Kontakts, basierend auf einer bestimmten Argument anzeigen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="a4b7b-124">Explorer oder Inspektor</span><span class="sxs-lookup"><span data-stu-id="a4b7b-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="a4b7b-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="a4b7b-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="a4b7b-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="a4b7b-127">Verwendet, um die Ereignisbehandlung aus der **IDispatch:: Invoke** -Funktion, die vor einem Druckvorgang ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="a4b7b-128">Anwendung</span><span class="sxs-lookup"><span data-stu-id="a4b7b-128">Application</span></span>  <br/> |
|<span data-ttu-id="a4b7b-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="a4b7b-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="a4b7b-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="a4b7b-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="a4b7b-131">Verwendet, um die Ereignisbehandlung aus der **IDispatch:: Invoke** -Funktion, die ausgelöst wird, wenn Outlook abgeschlossen ist, lesen die Eigenschaften des Elements.</span><span class="sxs-lookup"><span data-stu-id="a4b7b-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="a4b7b-132">Objekte auf Elementebene</span><span class="sxs-lookup"><span data-stu-id="a4b7b-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4b7b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4b7b-133">See also</span></span>

- [<span data-ttu-id="a4b7b-134">Aus Outlook exportierte APIs</span><span class="sxs-lookup"><span data-stu-id="a4b7b-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="a4b7b-135">Informationen zu von Outlook exportierten APIs</span><span class="sxs-lookup"><span data-stu-id="a4b7b-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="a4b7b-136">Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde</span><span class="sxs-lookup"><span data-stu-id="a4b7b-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="a4b7b-137">Gibt an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) anzeigen</span><span class="sxs-lookup"><span data-stu-id="a4b7b-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/de-de/library/office/gg262879.aspx)
- [<span data-ttu-id="a4b7b-138">Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="a4b7b-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

