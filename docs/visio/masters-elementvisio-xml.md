---
title: Masters-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Enthält die Master-Elemente für das Dokument.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538053"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="2bbcb-103">Masters-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2bbcb-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="2bbcb-104">Enthält die Master-Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2bbcb-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2bbcb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bbcb-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2bbcb-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="2bbcb-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2bbcb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2bbcb-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2bbcb-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2bbcb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2bbcb-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2bbcb-112">Masters. XML</span><span class="sxs-lookup"><span data-stu-id="2bbcb-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2bbcb-113">Definition</span><span class="sxs-lookup"><span data-stu-id="2bbcb-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2bbcb-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2bbcb-114">Elements and attributes</span></span>

<span data-ttu-id="2bbcb-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2bbcb-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2bbcb-116">Parent elements</span></span>

<span data-ttu-id="2bbcb-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2bbcb-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2bbcb-118">Child elements</span></span>

|<span data-ttu-id="2bbcb-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-119">**Element**</span></span>|<span data-ttu-id="2bbcb-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-120">**Type**</span></span>|<span data-ttu-id="2bbcb-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2bbcb-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2bbcb-122">Master</span><span class="sxs-lookup"><span data-stu-id="2bbcb-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2bbcb-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="2bbcb-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2bbcb-124">Enthält Elemente, die einen Master für das Dokument definieren.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="2bbcb-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="2bbcb-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2bbcb-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="2bbcb-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2bbcb-127">Gibt eine im Dokument definierte Master Verknüpfung an.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2bbcb-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="2bbcb-128">Attributes</span></span>

<span data-ttu-id="2bbcb-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="2bbcb-129">None.</span></span>
  

