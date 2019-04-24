---
title: DataConnection-Element (DataConnections_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrahiert die Kommunikation zwischen einem oder mehreren dataRecordset-Elementen und einer nicht-XML-Datenquelle.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344625"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="9f012-103">DataConnection-Element (DataConnections_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9f012-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9f012-104">Abstrahiert die Kommunikation zwischen einem oder mehreren \*\*\*\* DataRecordset-Elementen und einer nicht-XML-Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="9f012-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9f012-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9f012-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f012-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9f012-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9f012-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="9f012-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9f012-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f012-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9f012-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9f012-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9f012-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="9f012-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9f012-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="9f012-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9f012-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="9f012-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f012-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9f012-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9f012-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9f012-114">Elements and attributes</span></span>

<span data-ttu-id="9f012-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9f012-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9f012-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f012-116">Parent elements</span></span>

|<span data-ttu-id="9f012-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f012-117">**Element**</span></span>|<span data-ttu-id="9f012-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f012-118">**Type**</span></span>|<span data-ttu-id="9f012-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f012-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f012-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="9f012-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="9f012-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="9f012-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9f012-122">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="9f012-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9f012-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f012-123">Child elements</span></span>

<span data-ttu-id="9f012-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="9f012-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f012-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f012-125">Attributes</span></span>

|<span data-ttu-id="9f012-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9f012-126">**Attribute**</span></span>|<span data-ttu-id="9f012-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f012-127">**Type**</span></span>|<span data-ttu-id="9f012-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9f012-128">**Required**</span></span>|<span data-ttu-id="9f012-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f012-129">**Description**</span></span>|<span data-ttu-id="9f012-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9f012-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f012-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="9f012-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="9f012-132">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9f012-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9f012-133">Optional</span><span class="sxs-lookup"><span data-stu-id="9f012-133">optional</span></span>  <br/> |<span data-ttu-id="9f012-134">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="9f012-134">The default value is false.</span></span> <span data-ttu-id="9f012-135">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="9f012-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="9f012-136">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9f012-137">Befehl</span><span class="sxs-lookup"><span data-stu-id="9f012-137">Command</span></span>  <br/> |<span data-ttu-id="9f012-138">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f012-138">xsd:string</span></span>  <br/> |<span data-ttu-id="9f012-139">Optional</span><span class="sxs-lookup"><span data-stu-id="9f012-139">optional</span></span>  <br/> |<span data-ttu-id="9f012-140">Die Befehlszeichenfolge, die zum Abfragen der Datenquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f012-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="9f012-141">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f012-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9f012-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="9f012-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f012-143">xsd:string</span></span>  <br/> |<span data-ttu-id="9f012-144">Optional</span><span class="sxs-lookup"><span data-stu-id="9f012-144">optional</span></span>  <br/> |<span data-ttu-id="9f012-145">Die Verbindungszeichenfolge, die die Parameter definiert, die zum Herstellen einer Verbindung mit einer Datenquelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f012-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="9f012-146">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f012-147">FileName</span><span class="sxs-lookup"><span data-stu-id="9f012-147">FileName</span></span>  <br/> |<span data-ttu-id="9f012-148">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f012-148">xsd:string</span></span>  <br/> |<span data-ttu-id="9f012-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9f012-149">required</span></span>  <br/> |<span data-ttu-id="9f012-150">Der Name der Verbindungsdatei.</span><span class="sxs-lookup"><span data-stu-id="9f012-150">The name of the connection file.</span></span> <span data-ttu-id="9f012-151">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="9f012-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="9f012-152">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f012-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9f012-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="9f012-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f012-154">xsd:string</span></span>  <br/> |<span data-ttu-id="9f012-155">Optional</span><span class="sxs-lookup"><span data-stu-id="9f012-155">optional</span></span>  <br/> |<span data-ttu-id="9f012-156">Ein vom Benutzer bereitgestellter Name für die Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="9f012-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="9f012-157">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f012-158">ID</span><span class="sxs-lookup"><span data-stu-id="9f012-158">ID</span></span>  <br/> |<span data-ttu-id="9f012-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f012-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f012-160">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9f012-160">required</span></span>  <br/> |<span data-ttu-id="9f012-161">Die von Visio für eine bestimmte Verbindung zugewiesene ID, die innerhalb des Dokuments eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="9f012-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="9f012-162">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f012-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="9f012-163">Timeout</span></span>  <br/> |<span data-ttu-id="9f012-164">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f012-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f012-165">Optional</span><span class="sxs-lookup"><span data-stu-id="9f012-165">optional</span></span>  <br/> |<span data-ttu-id="9f012-166">Die Wartezeit in Minuten, während versucht wird, eine Verbindung herzustellen, bevor der Versuch beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f012-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="9f012-167">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f012-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

