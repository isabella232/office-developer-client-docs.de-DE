---
title: PidTagRoamingDictionary (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400327"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="38463-103">PidTagRoamingDictionary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="38463-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="38463-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38463-105">Enthält ein XML-Dokument, das Wörterbuch für die roaming beschreibt.</span><span class="sxs-lookup"><span data-stu-id="38463-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38463-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="38463-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38463-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="38463-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="38463-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="38463-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38463-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="38463-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="38463-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="38463-110">Data type:</span></span>  <br/> |<span data-ttu-id="38463-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="38463-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="38463-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="38463-112">Area:</span></span>  <br/> |<span data-ttu-id="38463-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="38463-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38463-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38463-114">Remarks</span></span>

<span data-ttu-id="38463-115">Diese Eigenschaft enthält einen UNICODE-XML-Dokument, die die UTF8-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="38463-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="38463-116">Eine Nachricht mit einem Wörterbuch Stream muss diese Eigenschaft mit dem folgenden Schema festlegen:</span><span class="sxs-lookup"><span data-stu-id="38463-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
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

<span data-ttu-id="38463-117">Es folgt eine Beispiel-XML-Dokument in dieser Eigenschaft auf eine Nachricht Konfigurationsdaten gespeichert:</span><span class="sxs-lookup"><span data-stu-id="38463-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="38463-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38463-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38463-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="38463-119">Protocol specifications</span></span>

<span data-ttu-id="38463-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38463-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38463-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="38463-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38463-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38463-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38463-123">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="38463-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38463-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="38463-124">Header files</span></span>

<span data-ttu-id="38463-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38463-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="38463-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="38463-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="38463-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38463-127">Mapitags.h</span></span>
  
> <span data-ttu-id="38463-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="38463-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38463-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38463-129">See also</span></span>



[<span data-ttu-id="38463-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38463-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38463-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38463-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38463-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="38463-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38463-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="38463-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

