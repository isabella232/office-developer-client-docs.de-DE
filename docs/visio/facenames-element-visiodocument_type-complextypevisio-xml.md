---
title: FaceNames-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Enthält eine Auflistung von FaceName-Elementen.
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539713"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="b669c-103">FaceNames-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b669c-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b669c-104">Enthält eine Auflistung von **FaceName** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="b669c-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b669c-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b669c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b669c-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b669c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b669c-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="b669c-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b669c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b669c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b669c-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b669c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b669c-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b669c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b669c-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="b669c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b669c-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="b669c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b669c-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b669c-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b669c-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b669c-114">Elements and attributes</span></span>

<span data-ttu-id="b669c-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b669c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b669c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b669c-116">Parent elements</span></span>

|<span data-ttu-id="b669c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b669c-117">**Element**</span></span>|<span data-ttu-id="b669c-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b669c-118">**Type**</span></span>|<span data-ttu-id="b669c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b669c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b669c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="b669c-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="b669c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="b669c-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b669c-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="b669c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b669c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b669c-123">Child elements</span></span>

|<span data-ttu-id="b669c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b669c-124">**Element**</span></span>|<span data-ttu-id="b669c-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b669c-125">**Type**</span></span>|<span data-ttu-id="b669c-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b669c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b669c-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="b669c-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b669c-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="b669c-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b669c-129">Enthält Informationen zu einer Schriftart.</span><span class="sxs-lookup"><span data-stu-id="b669c-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b669c-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="b669c-130">Attributes</span></span>

<span data-ttu-id="b669c-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="b669c-131">None.</span></span>
  

