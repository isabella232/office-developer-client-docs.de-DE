---
title: Kanonische PidTagRoamingDatatypes-Eigenschaft
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
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794990"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="93062-103">Kanonische PidTagRoamingDatatypes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93062-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="93062-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93062-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93062-105">Enthält eine Bitmaske dar, die angibt, welche Stream Eigenschaften für die Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="93062-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93062-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93062-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93062-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="93062-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="93062-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="93062-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93062-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="93062-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="93062-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93062-110">Data type:</span></span>  <br/> |<span data-ttu-id="93062-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93062-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93062-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93062-112">Area:</span></span>  <br/> |<span data-ttu-id="93062-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="93062-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93062-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93062-114">Remarks</span></span>

<span data-ttu-id="93062-115">Diese Eigenschaft muss auf eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="93062-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="93062-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="93062-116">**Value**</span></span>|<span data-ttu-id="93062-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93062-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93062-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="93062-118">0x00000002</span></span>  <br/> |<span data-ttu-id="93062-119">Gibt an, dass die Nachricht Ordner verknüpften Informationen (FAI) einen Wörterbuch-Stream in einem festen XML-Schema serialisiert und in der Eigenschaft **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) gespeichert enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="93062-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="93062-120">Wenn FAI-Nachricht keinen Wörterbuch Stream enthält, muss die Anwendung das Wörterbuch behandelt, als müssen keine Einträge.</span><span class="sxs-lookup"><span data-stu-id="93062-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="93062-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="93062-121">0x00000004</span></span>  <br/> |<span data-ttu-id="93062-122">Gibt an, dass die Nachricht FAI in die **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft, die eine beliebige XML-Schema verwendet gespeicherten XML-Stream enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="93062-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="93062-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93062-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93062-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93062-124">Protocol specifications</span></span>

<span data-ttu-id="93062-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93062-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93062-126">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="93062-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93062-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93062-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93062-128">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="93062-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93062-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="93062-129">Header files</span></span>

<span data-ttu-id="93062-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93062-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="93062-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93062-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="93062-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93062-132">Mapitags.h</span></span>
  
> <span data-ttu-id="93062-133">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="93062-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93062-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93062-134">See also</span></span>



[<span data-ttu-id="93062-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93062-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93062-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93062-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93062-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93062-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93062-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93062-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

