---
title: Masters-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Das Master-Shape enthält Elemente für das Dokument.
ms.openlocfilehash: d40071c64dc454eeb92f8518f89ef4de8b3b0cb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797446"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="6b8ae-103">Masters-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6b8ae-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="6b8ae-104">Das Master-Shape enthält Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b8ae-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6b8ae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b8ae-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b8ae-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="6b8ae-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b8ae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b8ae-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b8ae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6b8ae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b8ae-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b8ae-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="6b8ae-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b8ae-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6b8ae-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b8ae-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6b8ae-114">Elements and attributes</span></span>

<span data-ttu-id="6b8ae-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b8ae-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b8ae-116">Parent elements</span></span>

<span data-ttu-id="6b8ae-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b8ae-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b8ae-118">Child elements</span></span>

|<span data-ttu-id="6b8ae-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-119">**Element**</span></span>|<span data-ttu-id="6b8ae-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-120">**Type**</span></span>|<span data-ttu-id="6b8ae-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b8ae-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b8ae-122">Master</span><span class="sxs-lookup"><span data-stu-id="6b8ae-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b8ae-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="6b8ae-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b8ae-124">Enthält Elemente, die ein Master-Shape für das Dokument zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="6b8ae-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="6b8ae-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b8ae-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="6b8ae-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b8ae-127">Gibt ein master-Verknüpfung im Dokument definierten an.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6b8ae-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="6b8ae-128">Attributes</span></span>

<span data-ttu-id="6b8ae-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-129">None.</span></span>
  

