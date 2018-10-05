---
title: Rel-Element (Master_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Gibt eine Beziehung mit einem Webpart mit der entsprechenden master XML.
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393047"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="243d5-103">Rel-Element (Master_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="243d5-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="243d5-104">Gibt eine Beziehung mit einem Webpart mit der entsprechenden master XML.</span><span class="sxs-lookup"><span data-stu-id="243d5-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="243d5-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="243d5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="243d5-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="243d5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="243d5-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="243d5-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="243d5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="243d5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="243d5-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="243d5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="243d5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="243d5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="243d5-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="243d5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="243d5-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="243d5-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="243d5-113">Definition</span><span class="sxs-lookup"><span data-stu-id="243d5-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="243d5-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="243d5-114">Elements and attributes</span></span>

<span data-ttu-id="243d5-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="243d5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="243d5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="243d5-116">Parent elements</span></span>

|<span data-ttu-id="243d5-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="243d5-117">**Element**</span></span>|<span data-ttu-id="243d5-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="243d5-118">**Type**</span></span>|<span data-ttu-id="243d5-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="243d5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="243d5-120">Master</span><span class="sxs-lookup"><span data-stu-id="243d5-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="243d5-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="243d5-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="243d5-122">Gibt eine Instanz des Master-Shape in der Zeichnung gespeicherten XML-Code.</span><span class="sxs-lookup"><span data-stu-id="243d5-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="243d5-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="243d5-123">Child elements</span></span>

<span data-ttu-id="243d5-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="243d5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="243d5-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="243d5-125">Attributes</span></span>

|<span data-ttu-id="243d5-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="243d5-126">**Attribute**</span></span>|<span data-ttu-id="243d5-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="243d5-127">**Type**</span></span>|<span data-ttu-id="243d5-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="243d5-128">**Required**</span></span>|<span data-ttu-id="243d5-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="243d5-129">**Description**</span></span>|<span data-ttu-id="243d5-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="243d5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="243d5-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="243d5-131">r:id</span></span>  <br/> |<span data-ttu-id="243d5-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="243d5-132">xsd:string</span></span>  <br/> <span data-ttu-id="243d5-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="243d5-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="243d5-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="243d5-134">required</span></span>  <br/> |<span data-ttu-id="243d5-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="243d5-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="243d5-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="243d5-136">"rId#"</span></span>  <br/> <span data-ttu-id="243d5-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="243d5-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="243d5-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="243d5-138">Remarks</span></span>

<span data-ttu-id="243d5-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="243d5-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="243d5-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="243d5-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="243d5-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="243d5-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="243d5-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="243d5-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

