---
title: Rel-Element (Page_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Gibt eine Beziehung mit einem Webpart mit der entsprechenden Seite XML.
ms.openlocfilehash: 7a45764817175f670cdb009157e21a1a25f31cc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398906"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="7fbb4-103">Rel-Element (Page_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7fbb4-103">Rel element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7fbb4-104">Gibt eine Beziehung mit einem Webpart mit der entsprechenden Seite XML.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fbb4-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7fbb4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fbb4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7fbb4-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="7fbb4-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7fbb4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7fbb4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7fbb4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7fbb4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7fbb4-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7fbb4-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="7fbb4-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fbb4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7fbb4-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7fbb4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7fbb4-114">Elements and attributes</span></span>

<span data-ttu-id="7fbb4-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7fbb4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fbb4-116">Parent elements</span></span>

|<span data-ttu-id="7fbb4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-117">**Element**</span></span>|<span data-ttu-id="7fbb4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-118">**Type**</span></span>|<span data-ttu-id="7fbb4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7fbb4-120">Page</span><span class="sxs-lookup"><span data-stu-id="7fbb4-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7fbb4-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="7fbb4-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7fbb4-122">Gibt eine Instanz der Seite, die in der Zeichnung XML gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fbb4-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fbb4-123">Child elements</span></span>

<span data-ttu-id="7fbb4-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fbb4-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fbb4-125">Attributes</span></span>

|<span data-ttu-id="7fbb4-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-126">**Attribute**</span></span>|<span data-ttu-id="7fbb4-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-127">**Type**</span></span>|<span data-ttu-id="7fbb4-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-128">**Required**</span></span>|<span data-ttu-id="7fbb4-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-129">**Description**</span></span>|<span data-ttu-id="7fbb4-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7fbb4-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="7fbb4-131">r:id</span></span>  <br/> |<span data-ttu-id="7fbb4-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7fbb4-132">xsd:string</span></span>  <br/> <span data-ttu-id="7fbb4-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="7fbb4-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="7fbb4-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7fbb4-134">required</span></span>  <br/> |<span data-ttu-id="7fbb4-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="7fbb4-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="7fbb4-136">"rId#"</span></span>  <br/> <span data-ttu-id="7fbb4-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="7fbb4-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fbb4-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fbb4-138">Remarks</span></span>

<span data-ttu-id="7fbb4-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="7fbb4-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="7fbb4-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="7fbb4-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="7fbb4-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="7fbb4-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

