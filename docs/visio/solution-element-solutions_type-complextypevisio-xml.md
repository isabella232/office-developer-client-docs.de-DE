---
title: Solution-Element (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Gibt eine Instanz von Lösungs-XML an, die in der Zeichnung gespeichert ist.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540266"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a><span data-ttu-id="340e3-103">Solution-Element (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="340e3-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="340e3-104">Gibt eine Instanz von Lösungs-XML an, die in der Zeichnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="340e3-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="340e3-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="340e3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="340e3-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="340e3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="340e3-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="340e3-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="340e3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="340e3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="340e3-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="340e3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="340e3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="340e3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="340e3-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="340e3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="340e3-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="340e3-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="340e3-113">Definition</span><span class="sxs-lookup"><span data-stu-id="340e3-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="340e3-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="340e3-114">Elements and attributes</span></span>

<span data-ttu-id="340e3-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="340e3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="340e3-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="340e3-116">Parent elements</span></span>

|<span data-ttu-id="340e3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="340e3-117">**Element**</span></span>|<span data-ttu-id="340e3-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="340e3-118">**Type**</span></span>|<span data-ttu-id="340e3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="340e3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="340e3-120">Lösungen</span><span class="sxs-lookup"><span data-stu-id="340e3-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="340e3-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="340e3-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="340e3-122">Speichert die Eigenschaften der im Dokument gespeicherten Lösungen.</span><span class="sxs-lookup"><span data-stu-id="340e3-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="340e3-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="340e3-123">Child elements</span></span>

|<span data-ttu-id="340e3-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="340e3-124">**Element**</span></span>|<span data-ttu-id="340e3-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="340e3-125">**Type**</span></span>|<span data-ttu-id="340e3-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="340e3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="340e3-127">Rel</span><span class="sxs-lookup"><span data-stu-id="340e3-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="340e3-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="340e3-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="340e3-129">Gibt die Beziehung zu einem Teil mit der Lösungs-XML an, die dieser Lösung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="340e3-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="340e3-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="340e3-130">Attributes</span></span>

|<span data-ttu-id="340e3-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="340e3-131">**Attribute**</span></span>|<span data-ttu-id="340e3-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="340e3-132">**Type**</span></span>|<span data-ttu-id="340e3-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="340e3-133">**Required**</span></span>|<span data-ttu-id="340e3-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="340e3-134">**Description**</span></span>|<span data-ttu-id="340e3-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="340e3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="340e3-136">Name</span><span class="sxs-lookup"><span data-stu-id="340e3-136">Name</span></span>  <br/> |<span data-ttu-id="340e3-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="340e3-137">xsd:string</span></span>  <br/> |<span data-ttu-id="340e3-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="340e3-138">required</span></span>  <br/> |<span data-ttu-id="340e3-139">Der Name der Lösung.</span><span class="sxs-lookup"><span data-stu-id="340e3-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="340e3-140">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="340e3-140">Values of the xsd:string type.</span></span>  <br/> |
   

