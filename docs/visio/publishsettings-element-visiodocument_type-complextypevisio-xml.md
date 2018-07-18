---
title: PublishSettings-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Gibt die Einstellungen, die verwendet werden, wenn das Diagramm mithilfe von Visio Services in Microsoft SharePoint Server 2013 geöffnet wird.
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797754"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="22022-103">PublishSettings-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="22022-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="22022-104">Gibt die Einstellungen, die verwendet werden, wenn das Diagramm mithilfe von Visio Services in Microsoft SharePoint Server 2013 geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="22022-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22022-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="22022-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22022-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="22022-106">**Element type**</span></span> <br/> |[<span data-ttu-id="22022-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="22022-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="22022-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="22022-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="22022-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="22022-109">**Schema file**</span></span> <br/> |<span data-ttu-id="22022-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="22022-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="22022-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="22022-111">**Document parts**</span></span> <br/> |<span data-ttu-id="22022-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="22022-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="22022-113">Definition</span><span class="sxs-lookup"><span data-stu-id="22022-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="22022-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="22022-114">Elements and attributes</span></span>

<span data-ttu-id="22022-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="22022-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="22022-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22022-116">Parent elements</span></span>

|<span data-ttu-id="22022-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="22022-117">**Element**</span></span>|<span data-ttu-id="22022-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="22022-118">**Type**</span></span>|<span data-ttu-id="22022-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22022-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22022-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="22022-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="22022-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="22022-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22022-122">Gibt Eigenschaften einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="22022-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22022-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22022-123">Child elements</span></span>

|<span data-ttu-id="22022-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="22022-124">**Element**</span></span>|<span data-ttu-id="22022-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="22022-125">**Type**</span></span>|<span data-ttu-id="22022-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22022-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22022-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="22022-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="22022-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="22022-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22022-129">Gibt an, ob ein Zeichenblatt im Browser mithilfe von Visio Services sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="22022-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="22022-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="22022-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="22022-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="22022-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22022-132">Gibt an, ob ein Recordset mit Visio Services aktualisierbare ist.</span><span class="sxs-lookup"><span data-stu-id="22022-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="22022-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="22022-133">Attributes</span></span>

<span data-ttu-id="22022-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="22022-134">None.</span></span>
  

