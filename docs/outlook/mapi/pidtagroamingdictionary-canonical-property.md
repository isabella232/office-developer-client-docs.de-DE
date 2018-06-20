---
title: Kanonische PidTagRoamingDictionary-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795003"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="c9151-103">Kanonische PidTagRoamingDictionary-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9151-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="c9151-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9151-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9151-105">Enthält ein XML-Dokument, das Wörterbuch für die roaming beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c9151-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9151-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c9151-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9151-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="c9151-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="c9151-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c9151-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9151-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="c9151-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="c9151-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c9151-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9151-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9151-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9151-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c9151-112">Area:</span></span>  <br/> |<span data-ttu-id="c9151-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c9151-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9151-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9151-114">Remarks</span></span>

<span data-ttu-id="c9151-115">Diese Eigenschaft enthält einen UNICODE-XML-Dokument, die die UTF8-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9151-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="c9151-116">Eine Nachricht mit einem Wörterbuch Stream muss diese Eigenschaft mit dem folgenden Schema festlegen:</span><span class="sxs-lookup"><span data-stu-id="c9151-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="c9151-117">Es folgt eine Beispiel-XML-Dokument in dieser Eigenschaft auf eine Nachricht Konfigurationsdaten gespeichert:</span><span class="sxs-lookup"><span data-stu-id="c9151-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="c9151-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c9151-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9151-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c9151-119">Protocol specifications</span></span>

<span data-ttu-id="c9151-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9151-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9151-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c9151-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9151-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9151-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9151-123">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="c9151-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9151-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c9151-124">Header files</span></span>

<span data-ttu-id="c9151-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9151-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9151-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c9151-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9151-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9151-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c9151-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c9151-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9151-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9151-129">See also</span></span>



[<span data-ttu-id="c9151-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9151-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9151-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9151-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9151-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c9151-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9151-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c9151-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

