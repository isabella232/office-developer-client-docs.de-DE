---
title: Rel-Element (ForeignData_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Gibt eine Beziehung zwischen einem Shape und eines Dokumentteils, das die mit dem Shape verknüpften Bilddaten enthält.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383443"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="0364f-103">Rel-Element (ForeignData_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0364f-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0364f-104">Gibt eine Beziehung zwischen einem Shape und eines Dokumentteils, das die mit dem Shape verknüpften Bilddaten enthält.</span><span class="sxs-lookup"><span data-stu-id="0364f-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0364f-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0364f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0364f-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="0364f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0364f-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="0364f-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0364f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0364f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0364f-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0364f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0364f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0364f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0364f-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="0364f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0364f-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="0364f-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0364f-113">Definition</span><span class="sxs-lookup"><span data-stu-id="0364f-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0364f-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0364f-114">Elements and attributes</span></span>

<span data-ttu-id="0364f-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0364f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0364f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0364f-116">Parent elements</span></span>

|<span data-ttu-id="0364f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0364f-117">**Element**</span></span>|<span data-ttu-id="0364f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0364f-118">**Type**</span></span>|<span data-ttu-id="0364f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0364f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0364f-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="0364f-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0364f-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="0364f-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0364f-122">Gibt eine Instanz von Bilddaten in der Zeichnung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0364f-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0364f-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0364f-123">Child elements</span></span>

<span data-ttu-id="0364f-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="0364f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0364f-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="0364f-125">Attributes</span></span>

|<span data-ttu-id="0364f-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0364f-126">**Attribute**</span></span>|<span data-ttu-id="0364f-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0364f-127">**Type**</span></span>|<span data-ttu-id="0364f-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0364f-128">**Required**</span></span>|<span data-ttu-id="0364f-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0364f-129">**Description**</span></span>|<span data-ttu-id="0364f-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0364f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0364f-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="0364f-131">r:id</span></span>  <br/> |<span data-ttu-id="0364f-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0364f-132">xsd:string</span></span>  <br/> <span data-ttu-id="0364f-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="0364f-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="0364f-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0364f-134">required</span></span>  <br/> |<span data-ttu-id="0364f-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="0364f-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="0364f-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="0364f-136">"rId#"</span></span>  <br/> <span data-ttu-id="0364f-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="0364f-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0364f-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0364f-138">Remarks</span></span>

<span data-ttu-id="0364f-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="0364f-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="0364f-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="0364f-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="0364f-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0364f-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="0364f-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="0364f-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

