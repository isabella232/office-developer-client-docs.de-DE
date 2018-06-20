---
title: Rel-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Gibt eine Beziehung mit einem Webpart mit dem zugehörigen Recordset und Daten Bindungsinformationen an.
ms.openlocfilehash: 1086f2e812fc4be4b291c7a783877f4ccd39c815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797791"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="abda3-103">Rel-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="abda3-103">Rel element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="abda3-104">Gibt eine Beziehung mit einem Webpart mit dem zugehörigen Recordset und Daten Bindungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="abda3-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abda3-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="abda3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abda3-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="abda3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="abda3-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="abda3-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="abda3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="abda3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="abda3-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="abda3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="abda3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="abda3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="abda3-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="abda3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="abda3-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="abda3-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="abda3-113">Definition</span><span class="sxs-lookup"><span data-stu-id="abda3-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="abda3-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="abda3-114">Elements and attributes</span></span>

<span data-ttu-id="abda3-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="abda3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="abda3-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abda3-116">Parent elements</span></span>

|<span data-ttu-id="abda3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="abda3-117">**Element**</span></span>|<span data-ttu-id="abda3-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="abda3-118">**Type**</span></span>|<span data-ttu-id="abda3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abda3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abda3-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="abda3-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="abda3-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="abda3-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abda3-122">Gibt eine Instanz eines Recordset-Objekt und in der Zeichnung gespeicherten Daten Bindungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="abda3-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abda3-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abda3-123">Child elements</span></span>

<span data-ttu-id="abda3-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="abda3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abda3-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="abda3-125">Attributes</span></span>

|<span data-ttu-id="abda3-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="abda3-126">**Attribute**</span></span>|<span data-ttu-id="abda3-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="abda3-127">**Type**</span></span>|<span data-ttu-id="abda3-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="abda3-128">**Required**</span></span>|<span data-ttu-id="abda3-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abda3-129">**Description**</span></span>|<span data-ttu-id="abda3-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="abda3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="abda3-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="abda3-131">r:id</span></span>  <br/> |<span data-ttu-id="abda3-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="abda3-132">xsd:string</span></span>  <br/> <span data-ttu-id="abda3-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="abda3-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="abda3-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="abda3-134">required</span></span>  <br/> |<span data-ttu-id="abda3-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="abda3-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="abda3-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="abda3-136">"rId#"</span></span>  <br/> <span data-ttu-id="abda3-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="abda3-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abda3-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="abda3-138">Remarks</span></span>

<span data-ttu-id="abda3-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="abda3-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="abda3-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="abda3-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="abda3-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="abda3-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="abda3-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="abda3-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

