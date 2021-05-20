---
title: Rel-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Gibt eine Beziehung zu einem Teil mit den zugeordneten Recordset- und Datenbindungsinformationen an.
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542863"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="f54dd-103">Rel-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f54dd-103">Rel element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f54dd-104">Gibt eine Beziehung zu einem Teil mit den zugeordneten Recordset- und Datenbindungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="f54dd-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f54dd-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f54dd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f54dd-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f54dd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f54dd-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f54dd-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f54dd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f54dd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f54dd-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f54dd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f54dd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f54dd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f54dd-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f54dd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f54dd-112">pages.xml, masters.xml, recordsets.xml, Seite#.xml, Master#.xml</span><span class="sxs-lookup"><span data-stu-id="f54dd-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f54dd-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f54dd-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f54dd-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f54dd-114">Elements and attributes</span></span>

<span data-ttu-id="f54dd-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f54dd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f54dd-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f54dd-116">Parent elements</span></span>

|<span data-ttu-id="f54dd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f54dd-117">**Element**</span></span>|<span data-ttu-id="f54dd-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f54dd-118">**Type**</span></span>|<span data-ttu-id="f54dd-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f54dd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f54dd-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="f54dd-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f54dd-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="f54dd-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f54dd-122">Gibt eine Instanz eines Recordset- und Datenbindungsinformationen an, die in der Zeichnung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f54dd-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f54dd-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f54dd-123">Child elements</span></span>

<span data-ttu-id="f54dd-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="f54dd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f54dd-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="f54dd-125">Attributes</span></span>

|<span data-ttu-id="f54dd-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f54dd-126">**Attribute**</span></span>|<span data-ttu-id="f54dd-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f54dd-127">**Type**</span></span>|<span data-ttu-id="f54dd-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f54dd-128">**Required**</span></span>|<span data-ttu-id="f54dd-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f54dd-129">**Description**</span></span>|<span data-ttu-id="f54dd-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f54dd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f54dd-131">r:id</span><span class="sxs-lookup"><span data-stu-id="f54dd-131">r:id</span></span>  <br/> |<span data-ttu-id="f54dd-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f54dd-132">xsd:string</span></span>  <br/> <span data-ttu-id="f54dd-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="f54dd-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f54dd-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f54dd-134">required</span></span>  <br/> |<span data-ttu-id="f54dd-135">Gibt eine Beziehung zu einem Teil an.</span><span class="sxs-lookup"><span data-stu-id="f54dd-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f54dd-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="f54dd-136">"rId#"</span></span>  <br/> <span data-ttu-id="f54dd-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="f54dd-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f54dd-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f54dd-138">Remarks</span></span>

<span data-ttu-id="f54dd-139">Der Wert des **r:id-Attributs** muss ein **ST_RelationshipID** sein.</span><span class="sxs-lookup"><span data-stu-id="f54dd-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f54dd-140">Der **ST_RelationshipID** ist eine Zeichenfolge im Format "rId#", wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="f54dd-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f54dd-141">Die Zahl muss zwischen allen gleichgeordneten Elementen des **Rel-Elements eindeutig** sein.</span><span class="sxs-lookup"><span data-stu-id="f54dd-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f54dd-142">Weitere Informationen zum ST_RelationshipID finden Sie in der [SPEZIFIKATION ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="f54dd-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

