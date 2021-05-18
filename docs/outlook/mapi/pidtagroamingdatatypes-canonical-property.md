---
title: PidTagRoamingDatatypes (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359556"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="9d774-103">PidTagRoamingDatatypes (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9d774-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="9d774-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d774-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d774-105">Enthält eine Bitmaske, die angibt, welche Streameigenschaften in der Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9d774-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d774-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9d774-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d774-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="9d774-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="9d774-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9d774-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d774-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="9d774-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="9d774-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9d774-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d774-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9d774-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9d774-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9d774-112">Area:</span></span>  <br/> |<span data-ttu-id="9d774-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9d774-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d774-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d774-114">Remarks</span></span>

<span data-ttu-id="9d774-115">Diese Eigenschaft muss auf einen oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9d774-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="9d774-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d774-116">**Value**</span></span>|<span data-ttu-id="9d774-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d774-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d774-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9d774-118">0x00000002</span></span>  <br/> |<span data-ttu-id="9d774-119">Gibt an, dass die #A0 (Folder Associated Information) einen Dictionary-Stream enthalten soll, der in ein festes **#A1** serialisiert und in der PR_ROAMING_DICTIONARY ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9d774-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="9d774-120">Wenn die FAI-Nachricht keinen Dictionary-Stream enthält, muss die Anwendung das Wörterbuch als einträgelos behandeln.</span><span class="sxs-lookup"><span data-stu-id="9d774-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="9d774-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9d774-121">0x00000004</span></span>  <br/> |<span data-ttu-id="9d774-122">Gibt an, dass die #A0 einen #A1 **enthalten muss,** der in der PR_ROAMING_XMLSTREAM ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft gespeichert ist, die ein beliebiges #A1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d774-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9d774-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d774-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d774-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9d774-124">Protocol specifications</span></span>

<span data-ttu-id="9d774-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d774-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d774-126">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9d774-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d774-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d774-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d774-128">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="9d774-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d774-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9d774-129">Header files</span></span>

<span data-ttu-id="9d774-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d774-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d774-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9d774-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d774-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d774-132">Mapitags.h</span></span>
  
> <span data-ttu-id="9d774-133">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9d774-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d774-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d774-134">See also</span></span>



[<span data-ttu-id="9d774-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d774-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d774-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9d774-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d774-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9d774-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d774-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9d774-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

