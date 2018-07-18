---
title: Rel-Element (Page_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Gibt eine Beziehung mit einem Webpart mit der entsprechenden Seite XML.
ms.openlocfilehash: 9fc42527d311faa66b0b4041a0f978818ee84595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797794"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="b4e46-103">Rel-Element (Page_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b4e46-103">Rel element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b4e46-104">Gibt eine Beziehung mit einem Webpart mit der entsprechenden Seite XML.</span><span class="sxs-lookup"><span data-stu-id="b4e46-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4e46-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b4e46-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4e46-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b4e46-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b4e46-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b4e46-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b4e46-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4e46-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b4e46-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b4e46-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b4e46-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b4e46-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b4e46-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="b4e46-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b4e46-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="b4e46-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4e46-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b4e46-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b4e46-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b4e46-114">Elements and attributes</span></span>

<span data-ttu-id="b4e46-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b4e46-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b4e46-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e46-116">Parent elements</span></span>

|<span data-ttu-id="b4e46-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4e46-117">**Element**</span></span>|<span data-ttu-id="b4e46-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b4e46-118">**Type**</span></span>|<span data-ttu-id="b4e46-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e46-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4e46-120">Page</span><span class="sxs-lookup"><span data-stu-id="b4e46-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4e46-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="b4e46-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b4e46-122">Gibt eine Instanz der Seite, die in der Zeichnung XML gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4e46-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4e46-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4e46-123">Child elements</span></span>

<span data-ttu-id="b4e46-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4e46-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4e46-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4e46-125">Attributes</span></span>

|<span data-ttu-id="b4e46-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b4e46-126">**Attribute**</span></span>|<span data-ttu-id="b4e46-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b4e46-127">**Type**</span></span>|<span data-ttu-id="b4e46-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b4e46-128">**Required**</span></span>|<span data-ttu-id="b4e46-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4e46-129">**Description**</span></span>|<span data-ttu-id="b4e46-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b4e46-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4e46-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="b4e46-131">r:id</span></span>  <br/> |<span data-ttu-id="b4e46-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b4e46-132">xsd:string</span></span>  <br/> <span data-ttu-id="b4e46-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="b4e46-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="b4e46-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e46-134">required</span></span>  <br/> |<span data-ttu-id="b4e46-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="b4e46-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="b4e46-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="b4e46-136">"rId#"</span></span>  <br/> <span data-ttu-id="b4e46-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="b4e46-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4e46-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4e46-138">Remarks</span></span>

<span data-ttu-id="b4e46-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="b4e46-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="b4e46-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="b4e46-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="b4e46-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b4e46-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="b4e46-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="b4e46-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

