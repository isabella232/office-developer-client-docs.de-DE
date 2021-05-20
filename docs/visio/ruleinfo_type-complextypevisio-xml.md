---
title: RuleInfo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541645"
---
# <a name="ruleinfo_type-complextype-visio-xml"></a><span data-ttu-id="ca92f-102">RuleInfo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ca92f-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ca92f-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ca92f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca92f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ca92f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ca92f-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ca92f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ca92f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ca92f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ca92f-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ca92f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ca92f-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ca92f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca92f-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ca92f-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca92f-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ca92f-110">Elements and attributes</span></span>

<span data-ttu-id="ca92f-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ca92f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ca92f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca92f-112">Child elements</span></span>

<span data-ttu-id="ca92f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca92f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca92f-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca92f-114">Attributes</span></span>

|<span data-ttu-id="ca92f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ca92f-115">**Attribute**</span></span>|<span data-ttu-id="ca92f-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ca92f-116">**Type**</span></span>|<span data-ttu-id="ca92f-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ca92f-117">**Required**</span></span>|<span data-ttu-id="ca92f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca92f-118">**Description**</span></span>|<span data-ttu-id="ca92f-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ca92f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca92f-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="ca92f-120">RuleID</span></span>  <br/> |<span data-ttu-id="ca92f-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca92f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca92f-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ca92f-122">required</span></span>  <br/> ||<span data-ttu-id="ca92f-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ca92f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca92f-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="ca92f-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="ca92f-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca92f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca92f-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ca92f-126">required</span></span>  <br/> ||<span data-ttu-id="ca92f-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ca92f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

