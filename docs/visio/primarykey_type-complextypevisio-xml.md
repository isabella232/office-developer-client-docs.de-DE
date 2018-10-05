---
title: PrimaryKey_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391367"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="e8944-102">PrimaryKey_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e8944-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e8944-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e8944-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8944-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e8944-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e8944-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e8944-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e8944-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e8944-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e8944-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e8944-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e8944-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e8944-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8944-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e8944-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e8944-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e8944-110">Elements and attributes</span></span>

<span data-ttu-id="e8944-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e8944-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e8944-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8944-112">Child elements</span></span>

|<span data-ttu-id="e8944-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8944-113">**Element**</span></span>|<span data-ttu-id="e8944-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e8944-114">**Type**</span></span>|<span data-ttu-id="e8944-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8944-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e8944-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="e8944-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e8944-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="e8944-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e8944-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8944-118">Attributes</span></span>

|<span data-ttu-id="e8944-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e8944-119">**Attribute**</span></span>|<span data-ttu-id="e8944-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e8944-120">**Type**</span></span>|<span data-ttu-id="e8944-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e8944-121">**Required**</span></span>|<span data-ttu-id="e8944-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8944-122">**Description**</span></span>|<span data-ttu-id="e8944-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e8944-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8944-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="e8944-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e8944-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="e8944-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e8944-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e8944-126">required</span></span>  <br/> ||<span data-ttu-id="e8944-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e8944-127">Values of the xsd:string type.</span></span>  <br/> |
   

