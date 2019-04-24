---
title: Konstanten (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Dieses Thema enthält Konstante Definitionen für APIs, die von Outlook exportiert werden.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319873"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="10c4a-103">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="10c4a-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="10c4a-104">Dieses Thema enthält Konstante Definitionen für APIs, die von Outlook exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="10c4a-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="10c4a-105">Definitionen für die Unterstützung von Zeit Zonen</span><span class="sxs-lookup"><span data-stu-id="10c4a-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="10c4a-106">Definitionen für die Kategorie-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="10c4a-106">Definitions for Category support</span></span>

|<span data-ttu-id="10c4a-107">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="10c4a-107">**Constant**</span></span>|<span data-ttu-id="10c4a-108">**Definition**</span><span class="sxs-lookup"><span data-stu-id="10c4a-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10c4a-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="10c4a-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="10c4a-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10c4a-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="10c4a-111">Verschiedene Dispatch-IDs</span><span class="sxs-lookup"><span data-stu-id="10c4a-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="10c4a-112">Outlook macht die folgenden Dispatch-IDs (DispIds) verfügbar, damit Entwickler [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) verwenden können, um auf die entsprechende Eigenschaft oder Methode zuzugreifen oder das entsprechende Ereignis abzuhören.</span><span class="sxs-lookup"><span data-stu-id="10c4a-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="10c4a-113">**Zugeordnete Konstante**</span><span class="sxs-lookup"><span data-stu-id="10c4a-113">**Associated constant**</span></span>|<span data-ttu-id="10c4a-114">**DISPID-Wert**</span><span class="sxs-lookup"><span data-stu-id="10c4a-114">**Dispid value**</span></span>|<span data-ttu-id="10c4a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10c4a-115">**Description**</span></span>|<span data-ttu-id="10c4a-116">**Entsprechende Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="10c4a-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10c4a-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="10c4a-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="10c4a-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="10c4a-118">0xF024</span></span>  <br/> |<span data-ttu-id="10c4a-119">Wird verwendet, um die entsprechende Eigenschaft eines Elements aufzurufen, um zu überprüfen, ob das Element geändert, aber nicht gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="10c4a-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="10c4a-120">Objekte auf Elementebene</span><span class="sxs-lookup"><span data-stu-id="10c4a-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="10c4a-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="10c4a-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="10c4a-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="10c4a-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="10c4a-123">Wird verwendet, um die entsprechende Methode im Explorer oder Inspector aufzurufen, um anzugeben, ob das Bild eines Kontakts basierend auf einem bestimmten Argument angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10c4a-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="10c4a-124">Explorer oder Inspektor</span><span class="sxs-lookup"><span data-stu-id="10c4a-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="10c4a-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="10c4a-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="10c4a-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="10c4a-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="10c4a-127">Wird verwendet, um das Ereignis aus der **IDispatch:: Invoke** -Funktion zu behandeln, die vor einem Druckvorgang ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="10c4a-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="10c4a-128">Anwendung</span><span class="sxs-lookup"><span data-stu-id="10c4a-128">Application</span></span>  <br/> |
|<span data-ttu-id="10c4a-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="10c4a-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="10c4a-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="10c4a-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="10c4a-131">Wird verwendet, um das Ereignis aus der **IDispatch:: Invoke** -Funktion zu behandeln, die ausgelöst wird, wenn Outlook die Eigenschaften des Elements gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="10c4a-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="10c4a-132">Objekte auf Elementebene</span><span class="sxs-lookup"><span data-stu-id="10c4a-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10c4a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10c4a-133">See also</span></span>

- [<span data-ttu-id="10c4a-134">Aus Outlook exportierte APIs</span><span class="sxs-lookup"><span data-stu-id="10c4a-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="10c4a-135">Informationen zu von Outlook exportierten APIs</span><span class="sxs-lookup"><span data-stu-id="10c4a-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="10c4a-136">Bestimmen Sie, ob ein Outlook-Element geändert, aber nicht gespeichert (Outlook 2013 Hilfs-Referenz) wurde</span><span class="sxs-lookup"><span data-stu-id="10c4a-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="10c4a-137">Geben Sie an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="10c4a-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="10c4a-138">Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="10c4a-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

