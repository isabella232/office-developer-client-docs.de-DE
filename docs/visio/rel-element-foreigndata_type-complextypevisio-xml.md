---
title: Rel-Element (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Gibt eine Beziehung zwischen einer Form und einem Dokumentteil an, die die dem Shape zugeordneten Bilddaten enthält.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542807"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="c4d97-103">Rel-Element (ForeignData_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c4d97-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c4d97-104">Gibt eine Beziehung zwischen einer Form und einem Dokumentteil an, die die dem Shape zugeordneten Bilddaten enthält.</span><span class="sxs-lookup"><span data-stu-id="c4d97-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4d97-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c4d97-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4d97-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c4d97-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c4d97-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c4d97-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c4d97-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4d97-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c4d97-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c4d97-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c4d97-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c4d97-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c4d97-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c4d97-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c4d97-112">Pages. XML, Masters. XML, Recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="c4d97-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4d97-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c4d97-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c4d97-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c4d97-114">Elements and attributes</span></span>

<span data-ttu-id="c4d97-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c4d97-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c4d97-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4d97-116">Parent elements</span></span>

|<span data-ttu-id="c4d97-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4d97-117">**Element**</span></span>|<span data-ttu-id="c4d97-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c4d97-118">**Type**</span></span>|<span data-ttu-id="c4d97-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4d97-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4d97-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="c4d97-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c4d97-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="c4d97-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c4d97-122">Gibt eine Instanz von Bild Daten an, die in der Zeichnung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c4d97-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4d97-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4d97-123">Child elements</span></span>

<span data-ttu-id="c4d97-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4d97-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4d97-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4d97-125">Attributes</span></span>

|<span data-ttu-id="c4d97-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c4d97-126">**Attribute**</span></span>|<span data-ttu-id="c4d97-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c4d97-127">**Type**</span></span>|<span data-ttu-id="c4d97-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c4d97-128">**Required**</span></span>|<span data-ttu-id="c4d97-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4d97-129">**Description**</span></span>|<span data-ttu-id="c4d97-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c4d97-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4d97-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="c4d97-131">r:id</span></span>  <br/> |<span data-ttu-id="c4d97-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c4d97-132">xsd:string</span></span>  <br/> <span data-ttu-id="c4d97-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="c4d97-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="c4d97-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c4d97-134">required</span></span>  <br/> |<span data-ttu-id="c4d97-135">Gibt eine Beziehung zu einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="c4d97-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="c4d97-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="c4d97-136">"rId#"</span></span>  <br/> <span data-ttu-id="c4d97-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="c4d97-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4d97-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4d97-138">Remarks</span></span>

<span data-ttu-id="c4d97-139">Der Wert des **r:ID** -Attributs muss ein **ST_RelationshipID** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="c4d97-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="c4d97-140">Der **ST_RelationshipID** -Typ ist eine Zeichenfolge, die im Format "rId #" sein muss, wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="c4d97-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="c4d97-141">Die Zahl muss unter allen gleichgeordneten Elementen des **rel** -Elements eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c4d97-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="c4d97-142">Weitere Informationen zum ST_RelationshipID-Typ finden Sie in der [Spezifikation ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="c4d97-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

