---
title: Solution-Element (Solutions_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798163"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="666d8-103">Solution-Element (Solutions_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="666d8-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="666d8-104">Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.</span><span class="sxs-lookup"><span data-stu-id="666d8-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="666d8-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="666d8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="666d8-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="666d8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="666d8-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="666d8-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="666d8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="666d8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="666d8-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="666d8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="666d8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="666d8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="666d8-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="666d8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="666d8-112">Solutions.Xml</span><span class="sxs-lookup"><span data-stu-id="666d8-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="666d8-113">Definition</span><span class="sxs-lookup"><span data-stu-id="666d8-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="666d8-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="666d8-114">Elements and attributes</span></span>

<span data-ttu-id="666d8-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="666d8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="666d8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="666d8-116">Parent elements</span></span>

|<span data-ttu-id="666d8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="666d8-117">**Element**</span></span>|<span data-ttu-id="666d8-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="666d8-118">**Type**</span></span>|<span data-ttu-id="666d8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="666d8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="666d8-120">Lösungen</span><span class="sxs-lookup"><span data-stu-id="666d8-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="666d8-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="666d8-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="666d8-122">Speichert die Eigenschaften der Lösungen im Dokument gespeichert.</span><span class="sxs-lookup"><span data-stu-id="666d8-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="666d8-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="666d8-123">Child elements</span></span>

|<span data-ttu-id="666d8-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="666d8-124">**Element**</span></span>|<span data-ttu-id="666d8-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="666d8-125">**Type**</span></span>|<span data-ttu-id="666d8-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="666d8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="666d8-127">Rel</span><span class="sxs-lookup"><span data-stu-id="666d8-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="666d8-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="666d8-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="666d8-129">Gibt die Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="666d8-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="666d8-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="666d8-130">Attributes</span></span>

|<span data-ttu-id="666d8-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="666d8-131">**Attribute**</span></span>|<span data-ttu-id="666d8-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="666d8-132">**Type**</span></span>|<span data-ttu-id="666d8-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="666d8-133">**Required**</span></span>|<span data-ttu-id="666d8-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="666d8-134">**Description**</span></span>|<span data-ttu-id="666d8-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="666d8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="666d8-136">Name</span><span class="sxs-lookup"><span data-stu-id="666d8-136">Name</span></span>  <br/> |<span data-ttu-id="666d8-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="666d8-137">xsd:string</span></span>  <br/> |<span data-ttu-id="666d8-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="666d8-138">required</span></span>  <br/> |<span data-ttu-id="666d8-139">Der Name der Lösung.</span><span class="sxs-lookup"><span data-stu-id="666d8-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="666d8-140">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="666d8-140">Values of the xsd:string type.</span></span>  <br/> |
   

