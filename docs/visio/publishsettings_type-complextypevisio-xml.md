---
title: PublishSettings_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 6e9974d35b904581d43f481a02b8a3adee811730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797753"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="8ced7-102">PublishSettings_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8ced7-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8ced7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="8ced7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ced7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ced7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8ced7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8ced7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8ced7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8ced7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8ced7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="8ced7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8ced7-108">Keine</span><span class="sxs-lookup"><span data-stu-id="8ced7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ced7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="8ced7-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ced7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8ced7-110">Elements and attributes</span></span>

<span data-ttu-id="8ced7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8ced7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8ced7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ced7-112">Child elements</span></span>

|<span data-ttu-id="8ced7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ced7-113">**Element**</span></span>|<span data-ttu-id="8ced7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ced7-114">**Type**</span></span>|<span data-ttu-id="8ced7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ced7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ced7-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="8ced7-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ced7-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="8ced7-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8ced7-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="8ced7-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ced7-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="8ced7-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8ced7-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ced7-120">Attributes</span></span>

<span data-ttu-id="8ced7-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ced7-121">None.</span></span>
  

