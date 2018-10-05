---
title: DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Fasst die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer nicht auf XML basierenden Datenquelle zusammen.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399424"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="ded59-103">DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ded59-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ded59-104">Fasst die Kommunikation zwischen einem oder mehreren **DataRecordset** -Elementen und einer nicht auf XML basierenden Datenquelle zusammen.</span><span class="sxs-lookup"><span data-stu-id="ded59-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ded59-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ded59-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ded59-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ded59-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ded59-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="ded59-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ded59-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ded59-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ded59-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ded59-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ded59-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ded59-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ded59-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="ded59-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ded59-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="ded59-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ded59-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ded59-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ded59-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ded59-114">Elements and attributes</span></span>

<span data-ttu-id="ded59-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ded59-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ded59-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ded59-116">Parent elements</span></span>

|<span data-ttu-id="ded59-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ded59-117">**Element**</span></span>|<span data-ttu-id="ded59-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ded59-118">**Type**</span></span>|<span data-ttu-id="ded59-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ded59-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ded59-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="ded59-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="ded59-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="ded59-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ded59-122">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="ded59-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ded59-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ded59-123">Child elements</span></span>

<span data-ttu-id="ded59-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="ded59-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ded59-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="ded59-125">Attributes</span></span>

|<span data-ttu-id="ded59-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ded59-126">**Attribute**</span></span>|<span data-ttu-id="ded59-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ded59-127">**Type**</span></span>|<span data-ttu-id="ded59-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ded59-128">**Required**</span></span>|<span data-ttu-id="ded59-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ded59-129">**Description**</span></span>|<span data-ttu-id="ded59-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ded59-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ded59-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="ded59-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="ded59-132">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ded59-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ded59-133">Optional</span><span class="sxs-lookup"><span data-stu-id="ded59-133">optional</span></span>  <br/> |<span data-ttu-id="ded59-134">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="ded59-134">The default value is false.</span></span> <span data-ttu-id="ded59-135">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="ded59-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="ded59-136">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ded59-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ded59-137">Command</span><span class="sxs-lookup"><span data-stu-id="ded59-137">Command</span></span>  <br/> |<span data-ttu-id="ded59-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ded59-138">xsd:string</span></span>  <br/> |<span data-ttu-id="ded59-139">Optional</span><span class="sxs-lookup"><span data-stu-id="ded59-139">optional</span></span>  <br/> |<span data-ttu-id="ded59-140">Die Befehlszeichenfolge wird zum Abfragen der Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ded59-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="ded59-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ded59-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ded59-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ded59-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="ded59-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ded59-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ded59-144">Optional</span><span class="sxs-lookup"><span data-stu-id="ded59-144">optional</span></span>  <br/> |<span data-ttu-id="ded59-145">Die Verbindungszeichenfolge, die die Verbindung zu einer Datenquelle erforderlichen Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="ded59-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="ded59-146">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ded59-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ded59-147">FileName</span><span class="sxs-lookup"><span data-stu-id="ded59-147">FileName</span></span>  <br/> |<span data-ttu-id="ded59-148">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ded59-148">xsd:string</span></span>  <br/> |<span data-ttu-id="ded59-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ded59-149">required</span></span>  <br/> |<span data-ttu-id="ded59-150">Der Name der Verbindungsdatei.</span><span class="sxs-lookup"><span data-stu-id="ded59-150">The name of the connection file.</span></span> <span data-ttu-id="ded59-151">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="ded59-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="ded59-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ded59-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ded59-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ded59-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="ded59-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ded59-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ded59-155">Optional</span><span class="sxs-lookup"><span data-stu-id="ded59-155">optional</span></span>  <br/> |<span data-ttu-id="ded59-156">Ein Benutzer zur Verfügung gestellten Name für die Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="ded59-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="ded59-157">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ded59-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ded59-158">ID</span><span class="sxs-lookup"><span data-stu-id="ded59-158">ID</span></span>  <br/> |<span data-ttu-id="ded59-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ded59-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ded59-160">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ded59-160">required</span></span>  <br/> |<span data-ttu-id="ded59-161">Die ID für eine angegebene Verbindung, die innerhalb des Dokuments eindeutig von Visio zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ded59-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="ded59-162">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ded59-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ded59-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="ded59-163">Timeout</span></span>  <br/> |<span data-ttu-id="ded59-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ded59-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ded59-165">Optional</span><span class="sxs-lookup"><span data-stu-id="ded59-165">optional</span></span>  <br/> |<span data-ttu-id="ded59-166">Die Wartezeit in Minuten beim Versuch, bevor der Versuch beendet eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ded59-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="ded59-167">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ded59-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

