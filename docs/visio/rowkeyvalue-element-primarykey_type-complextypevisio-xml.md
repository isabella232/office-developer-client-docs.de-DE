---
title: RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordsets an.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538130"
---
# <a name="rowkeyvalue-element-primarykey_type-complextype-visio-xml"></a><span data-ttu-id="58af2-103">RowKeyValue-Element (PrimaryKey_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="58af2-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="58af2-104">Gibt den Wert eines Primärschlüssels für eine einzelne Zeile eines Recordsets an.</span><span class="sxs-lookup"><span data-stu-id="58af2-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58af2-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="58af2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58af2-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="58af2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="58af2-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="58af2-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="58af2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="58af2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="58af2-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="58af2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="58af2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="58af2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="58af2-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="58af2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="58af2-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="58af2-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58af2-113">Definition</span><span class="sxs-lookup"><span data-stu-id="58af2-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58af2-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="58af2-114">Elements and attributes</span></span>

<span data-ttu-id="58af2-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="58af2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="58af2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58af2-116">Parent elements</span></span>

|<span data-ttu-id="58af2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="58af2-117">**Element**</span></span>|<span data-ttu-id="58af2-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58af2-118">**Type**</span></span>|<span data-ttu-id="58af2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58af2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58af2-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="58af2-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58af2-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="58af2-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58af2-122">Gibt einen Primärschlüssel eines Recordsets an.</span><span class="sxs-lookup"><span data-stu-id="58af2-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58af2-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58af2-123">Child elements</span></span>

<span data-ttu-id="58af2-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="58af2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58af2-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="58af2-125">Attributes</span></span>

|<span data-ttu-id="58af2-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="58af2-126">**Attribute**</span></span>|<span data-ttu-id="58af2-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58af2-127">**Type**</span></span>|<span data-ttu-id="58af2-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="58af2-128">**Required**</span></span>|<span data-ttu-id="58af2-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58af2-129">**Description**</span></span>|<span data-ttu-id="58af2-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="58af2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58af2-131">RowID</span><span class="sxs-lookup"><span data-stu-id="58af2-131">RowID</span></span>  <br/> |<span data-ttu-id="58af2-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58af2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58af2-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58af2-133">required</span></span>  <br/> |<span data-ttu-id="58af2-134">Ein eindeutiger Wert, der eine Zeile eines Recordsets identifiziert.</span><span class="sxs-lookup"><span data-stu-id="58af2-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="58af2-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="58af2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58af2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="58af2-136">Value</span></span>  <br/> |<span data-ttu-id="58af2-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="58af2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="58af2-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58af2-138">required</span></span>  <br/> |<span data-ttu-id="58af2-139">Der Wert des Primärschlüssels für diese Zeile des Recordsets.</span><span class="sxs-lookup"><span data-stu-id="58af2-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="58af2-140">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="58af2-140">Values of the xsd:string type.</span></span>  <br/> |
   

