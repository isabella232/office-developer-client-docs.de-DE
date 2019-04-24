---
title: Kanonische Pidtagroamingdatatypes (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359556"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="db181-103">Kanonische Pidtagroamingdatatypes (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="db181-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="db181-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db181-105">Enthält eine Bitmaske, die angibt, welche Stream-Eigenschaften in der Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="db181-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db181-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="db181-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db181-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="db181-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="db181-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="db181-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db181-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="db181-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="db181-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="db181-110">Data type:</span></span>  <br/> |<span data-ttu-id="db181-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="db181-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="db181-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="db181-112">Area:</span></span>  <br/> |<span data-ttu-id="db181-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="db181-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db181-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db181-114">Remarks</span></span>

<span data-ttu-id="db181-115">Diese Eigenschaft muss auf einen oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="db181-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="db181-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="db181-116">**Value**</span></span>|<span data-ttu-id="db181-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db181-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db181-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="db181-118">0x00000002</span></span>  <br/> |<span data-ttu-id="db181-119">Gibt an, dass die Nachricht "Folder Associated Information" (FAI) einen Wörterbuchdaten Strom enthalten soll, der in ein festes XML-Schema serialisiert und in der **PR_ROAMING_DICTIONARY** ([pidtagroamingdictionary (](pidtagroamingdictionary-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="db181-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="db181-120">Wenn die FAI-Nachricht keinen Wörterbuchdaten Strom enthält, muss die Anwendung das Wörterbuch als keine Einträge behandeln.</span><span class="sxs-lookup"><span data-stu-id="db181-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="db181-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="db181-121">0x00000004</span></span>  <br/> |<span data-ttu-id="db181-122">Gibt an, dass die FAI-Nachricht einen in der **PR_ROAMING_XMLSTREAM** ([pidtagroamingxmlstream (](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft gespeicherten XML-Stream enthalten muss, der ein beliebiges XML-Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="db181-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="db181-123">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db181-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db181-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="db181-124">Protocol specifications</span></span>

<span data-ttu-id="db181-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db181-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db181-126">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="db181-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db181-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db181-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db181-128">Gibt den Speicherort und die Eigenschaften von Client-und Serverkonfigurationsdaten an, wie beispielsweise Listen mit freigegebenen Kategorien und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="db181-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db181-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="db181-129">Header files</span></span>

<span data-ttu-id="db181-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="db181-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="db181-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="db181-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="db181-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="db181-132">Mapitags.h</span></span>
  
> <span data-ttu-id="db181-133">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="db181-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db181-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db181-134">See also</span></span>



[<span data-ttu-id="db181-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db181-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db181-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db181-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db181-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="db181-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db181-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="db181-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

